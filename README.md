# ussd_golang

## How to run
1. Clone the repo
2. Run `go run main.go`
3. Open your postman and make a post request to `localhost:8080/ussd_callback`
4. Add the following json to the body of the request
    ```json
    {
        "sessionId": "123456789",
        "serviceCode": "*332*1234#",
        "phoneNumber": "254712345678",
        "text": "1"
    }
    ```

 **Note**<br />
The `text` field is the input from the user. It can be empty or have a value depending on the menu level.

To go to next page or next menu, add "*" in-between the previous input and the next input. For example, if the user is on the first menu and they want to go to the second menu, the `text` field should be `1*1`. If the user is on the second menu and they want to go to the third menu, the `text` field should be `1*1*1`.

#
![image](https://github.com/Josephchinedu/ussd_golang/blob/master/image.PNG?raw=true)