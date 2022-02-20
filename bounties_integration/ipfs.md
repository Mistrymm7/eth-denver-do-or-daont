# Web3.Storage Integration

```
import { Web3Storage } from 'web3.storage'
import { getFilesFromPath } from 'web3.storage'
import { File } from 'web3.storage'
import fetch from "node-fetch";


function getAccessToken() {
  // If you're just testing, you can paste in a token
  // and uncomment the following line:
  return 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiJkaWQ6ZXRocjoweDlBNENEOWUyYzdmMGNDOWEyRjczZjVGRmFiOTA2NTZiNzlDMjg3Y0MiLCJpc3MiOiJ3ZWIzLXN0b3JhZ2UiLCJpYXQiOjE2NDUzMjI4MTQxNTAsIm5hbWUiOiJIYWNrYXRob24ifQ.Gk_g92F3zez3JBhBujNOOrcl5hWYrYHzIYex9yfUmus'
  //return process.env.WEB3STORAGE_TOKEN
}

function makeStorageClient() {
  console.log("Test")
  return new Web3Storage({ token: getAccessToken() })
  
}

function makeFileObjects() {
  const obj = { hello: 'world' }
  console.log("Using buffer")
  //API Calls
  //Off-chain Governance API Calls

  let buffer;
    fetch("https://api.boardroom.info/v1/protocols", {
    headers: {
        Accept: "application/json"
    }
    }).then(response => 
    response.json()).then(data => 
    buffer = Buffer.from(JSON.stringify(data)));
    
    //console.log("API Fetch"));

    const files = [
        new File([buffer], 'protocols.json')
    ]
    return files

  
}

async function storeFiles(files) {
  const client = makeStorageClient()
  const cid = await client.put(files)
  console.log('stored files with cid:', cid)
  return cid
}

//storeFiles(makeFileObjects())

//Listing Latest Uploads to make Endpoint Query

async function listUploads() {
  const client = makeStorageClient()
  for await (const upload of client.list()) {
    console.log(`${upload.name} - cid: ${upload.cid} - size: ${upload.dagSize}`)
  }
}

//listUploads()

async function listWithLimits() {
  const client = makeStorageClient()

  // get today's date and subtract 1 day
  const d = new Date()
  //d.setDate(d.getDate() - 1)

  // the list method's before parameter accepts an ISO formatted string
  const before = d.toISOString()

  // limit to ten results
  const maxResults = 1

  for await (const upload of client.list({ before, maxResults })) {
    console.log(upload)
  }
}

// listWithLimits()

async function listLatestUploads() {
    const client = makeStorageClient()
    const uploadNames = []
    for await (const item of client.list()) {
        uploadNames.push(item.cid)
        //console.log(item)
    }

    console.log(uploadNames[0])
}

listLatestUploads() 

// Retrive Debugging Check

/* async function retrieve(cid) {
  const client = makeStorageClient()
  const res = await client.get(cid)
  console.log(`Got a response! [${res.status}] ${res.statusText}`)
  if (!res.ok) {
    throw new Error(`failed to get ${cid}`)
  }

  //console.log(res)

  // unpack File objects from the response
  const files = await res.files()
  for (const file of files) {
    console.log(`${file.cid} -- ${file.path} -- ${file.size}`)
  }

  // request succeeded! do something with the response object here...
} */

//retrieve('bafybeidjb4xq7qozjpcsrg6o43y5hx7a3y76yl44ukvrfgfucw5ssxm5ju')
//retrieve('bafybeiaggvf6vvzcohdsidesfb7zoonmqkza5krnnab6jdwkb32huhft54')


// Check Status of Upload
/* async function checkStatus(cid) {
  const client = makeStorageClient()
  const status = await client.status(cid)
  console.log(status)
  if (status) {
    // your code to do something fun with the status info here
  }
}

checkStatus('bafybeiaggvf6vvzcohdsidesfb7zoonmqkza5krnnab6jdwkb32huhft54') */


```












