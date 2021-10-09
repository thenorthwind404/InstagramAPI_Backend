The API consists of 5 major functions: CreateUserEndpoint( ), GetUserEndpoint( ), CreatePostEndpoint( ), GetpostEndpoint( ). 
<br/>  
CreateUserEndpoint( )<br/>
        Declare the response type to be JSON<br/>
        Declare the user object and store the request data in it<br/>
        Encrypt the password using SHA256<br/>
        Insert the object into MongoDB called InstagramDB and collection name Users<br/>
<br/><br/>
GetUserEndpoint( )<br/>
        Declare the response type to be JSON<br/>
        Get the request data<br/>
        Get ID from request data<br/>
        Use ID to find the data in MongoDB and store it into a user object.<br/>
<br/><br/>
CreatePostEndpoint( )<br/>
        Declare the response type to be JSON<br/>
        Declare a post object for struct posts<br/>
        Connect with collection “Posts”<br/>
        Get current date and time and format it using the time library and store it in post object<br/>
        Push the data into MongoDB<br/>
<br/><br/>
GetPostEndpoint()<br/>
        Declare the response type to be JSON<br/>
        Declare a post object for struct posts<br/>
        Get ID from the Get request type<br/>
        Connect with collection “Posts”<br/>
        Find the data using ID<br/>
        Our response is generated. Encode to JSON<br/>
<br/>        <br/>
GetAllPostsEndpoint()<br/>
        Declare the response type to be JSON<br/>
        Declare a post object slice<br/>
        Connect to collections<br/>
        Generate a cursor<br/>
        Create a temp Posts object<br/>
        Use cursor.Next( ) to get each data and save it in the temp object<br/>
        Append temp object to the post object slice<br/>
        Our response is generated. Encode it to JSON<br/>
