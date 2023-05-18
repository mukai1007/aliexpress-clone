# AliExpress Clone / (aliexpress-clone)

```
git clone https://github.com/mukai1007/aliexpress-clone.git

cp .env.example .env

npm i

npx prisma generate

npm run dev
```
You'll have to setup a Supabase account & Stripe account, then add all of the details in to your .env file.

Once you've connected your application to Supabase. You'll also need to setup the Auth Providers:
    Google [Google](https://cloud.google.com)
    Github [Github](https://github.com/settings/developers)
    
    https://supabase.com/docs/guides/auth/social-login/auth-google
    https://supabase.com/docs/guides/auth/social-login/auth-github
    
Now run the command to migrate your database tables and run your seed file.

```
npx prisma migrate dev --name init
```
# Application Images

<img width="1439" src="https://github.com/mukai1007/aliexpress-clone/blob/master/public/app-photo/home.png?raw=true">
<img width="1439" src="https://github.com/mukai1007/aliexpress-clone/blob/master/public/app-photo/search.png?raw=true">
<img width="1439" src="https://github.com/mukai1007/aliexpress-clone/blob/master/public/app-photo/detailview.png?raw=true">
<img width="1439" src="https://github.com/mukai1007/aliexpress-clone/blob/master/public/app-photo/cart.png?raw=true">
<img width="1439" src="https://github.com/mukai1007/aliexpress-clone/blob/master/public/app-photo/checkout.png?raw=true">
<img width="1439" src="https://github.com/mukai1007/aliexpress-clone/blob/master/public/app-photo/orders.png?raw=true">