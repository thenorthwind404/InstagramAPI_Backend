The API consists of 5 major functions: CreateUserEndpoint( ), GetUserEndpoint( ), CreatePostEndpoint( ), GetpostEndpoint( ). 
<br/>  
CreateUserEndpoint( )<br/>
        Declare the response type to be JSON
        Declare the user object and store the request data in it
        Encrypt the password using SHA256
        Insert the object into MongoDB called InstagramDB and collection name Users
<br/>
GetUserEndpoint( )<br/>
        Declare the response type to be JSON
        Get the request data
        Get ID from request data
        Use ID to find the data in MongoDB and store it into a user object.
<br/>
CreatePostEndpoint( )<br/>
        Declare the response type to be JSON
        Declare a post object for struct posts
        Connect with collection “Posts”
        Get current date and time and format it using the time library and store it in post object
        Push the data into MongoDB
<br/>
GetPostEndpoint()<br/>
        Declare the response type to be JSON
        Declare a post object for struct posts
        Get ID from the Get request type
        Connect with collection “Posts”
        Find the data using ID
        Our response is generated. Encode to JSON
<br/>        
GetAllPostsEndpoint()<br/>
        Declare the response type to be JSON
        Declare a post object slice
        Connect to collections
        Generate a cursor
        Create a temp Posts object
        Use cursor.Next( ) to get each data and save it in the temp object
        Append temp object to the post object slice
        Our response is generated. Encode it to JSON
