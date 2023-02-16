# Overview
Laravel multiple Admin and User roles authentication using <a href="https://laravel.com/docs/9.x/starter-kits#laravel-breeze" target="_blank">Laravel Breeze</a> Where User role can able login using their email address. OTP will be sent to email address for login authentication. Resend email OTP functionality also implement if timer expired.

Server Requirements
=====================================
<ul>
  <li><a href="https://www.php.net/" target="_blank">PHP Version</a> => 7.4 or higher</li>
  <li><a href="https://laravel.com/docs/master" target="_blank">Laravel Version</a> => 8 or higher</li>
  <li><a href="https://www.mysql.com/" target="_blank">MySQL Version</a> => 5.7 or higher</li>
</ul>

Setup Basic Commands
=====================================
1) git clone repository_url
2) cd laravel-breeze-web-guard-user-email-otp
3) composer update
4) create database and configure .env database connection
5) php artisan migrate
6) php artisan db:seed
7) php artisan serve

Routes Lists
=====================================
<ol>
  <li> Auth Routes </li>
  <ul>
    <li>User Login : http://127.0.0.1:8000/login </li>
    <li>User Register : http://127.0.0.1:8000/register </li>
    <li>Admin Login : http://127.0.0.1:8000/admin/login </li>
    <li>Admin Register : http://127.0.0.1:8000/admin/register </li>
  </ul>
</ol>

Credentials Details
=====================================
<b>User Role</b>
<ul>
  <li>Username : <a href="mailto:user@yopmail.com">user@yopmail.com</a></li>
  <li>Password : user@123456</li>
</ul>

<b>Admin Role</b>
<ul>
  <li>Username : <a href="mailto:admin@yopmail.com">admin@yopmail.com</a></li>
  <li>Password : admin@123456</li>
</ul>

Project Requirement 
=====================================
<ol>
  <li> Authentication Using Laravel Web Gaurd : </li>
  <li>Admin Role Requirement </li>
    <ul>
      <li> <b> Admin Registration Fields </b> </li>
      <li> Name : [ Validation Rules : Accept only strings and space, Required ] </li>
      <li> Email : [ Validation Rules : Accept only valid email address, Required ] </li>
      <li> Password : [ Validation Rules : Accept only valid password min 8 length with alphanumeric, Required ] </li>
      <li> Confirm Password : [ Validation Rules : should be same as Password field, Required ] </li>
      <li> On Registration button click redirect to Admin dashboard page </li>      
      <li> Generate 5 dummy sample for Admin role using Factory and Seeder </li>      
      <li> Make Seprate dashboard view ,admin table and Admin model </li>
      <li> <b> Admin Login Fields </b> </li>
      <li> Email : [ Validation Rules : Accept only valid email address, Required ] </li>
      <li> Password : [ Validation Rules : Accept only valid password min 8 length with alphanumeric, Required ] </li>
      <li> On Login button click redirect to Admin dashboard page if credential is validated </li>
    </ul>
  <li>User Role Requirement</li>
      <ul>
          <li> <b> User Registration Fields </b> </li>
          <li> Name : [ Validation Rules : Accept only strings and space, Required ] </li>
          <li> Email : [ Validation Rules : Accept only valid email address, Required ] </li>
          <li> Password : [ Validation Rules : Accept only valid password minimum 8 length with alphanumeric, Required ] </li>
          <li> Confirm Password : [ Validation Rules : should be same as Password field, Required ] </li>
          <li> On Registration button redirect to Login Page with successfull register message </li>                              
          <li> Generate 5 dummy sample for User role using Factory and Seeder </li>          
          <li> Make Seprate dashboard view ,user table and User model </li>
          <li> <b> User Login Fields </b> </li>
          <li> Email : [ Validation Rules : Accept only valid email address, Required ] </li>          
          <li> On Login button click New Verify OTP Page will be open with Enter OTP </li>
          <li> 1 minutes timer counter will shows to user </li>
          <li> After 1 minutes timer counter will shows Resend OTP button to user and should able to resend 8 digit OTP at registered email</li>
          <li> After 1 minutes timer counter old OTP will be expired and not allow to login with old OTP</li>
          <li> On Successfull OTP verification will redirect to home page </li>
      </ul>
</ol>

# Laravel / PHP Coding Standards
<ol>
 <li>Use Laravel's migration scripts for database schema and tables related to further all operations</li>
 <li>Use Laravel's factory and seeders for sample dummy data creations where required</li>
 <li>Use Laravel's validation using Request classes where required</li>
 <li>Use Laravel's Eloquent and Relationships in models where required</li>
 <li>Use camel case for function name and variable name. E.g getProductDetails() , $categoryDetails </li>
 <li>Comment on the above function with short details of that function use or purpose of function creation. </li>
 <li>Reuse the common codes using some helper class functions etc</li>
 <li>Remove unnecessary code and debug points that are not needed</li>
 <li>Avoid unnecessary loops if not required</li>
 <li>Avoid unnecessary variable creations</li>
 <li>Use PHP design patterns where required <a href="https://refactoring.guru/design-patterns/php" target="_blank">Design Patterns</a></li>    <li>Normalize database tables where required <a href="https://www.guru99.com/database-normalization.html" target="_blank">Database Normalization</a></li>
 <li>Optimize database tables</li>
 <li>Avoid MySQL joins queries if not required</li>
 <li>Avoid MySQL sub queries if it does not require</li>
 <li>For more information, please read the document <a href="https://drive.google.com/drive/folders/1_nxEPw01QnVkVQfZ2WtXyeX7NcQ6ENdh" target='_blank'>Code Standard</a>
</ol>
  
References : 
=====================================
a) https://www.youtube.com/watch?v=yXjHYTFRTC8

