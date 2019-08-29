```
export async function handler(event: any, context: any, callback: any) {
  console.log(JSON.stringify(event));
  return {
    statusCode: 200,
    body: "hello"
  };
}
```
