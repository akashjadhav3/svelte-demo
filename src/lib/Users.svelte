<script>
    import user2 from "../assets/images/user2.png";
    import user3 from "../assets/images/user3.png";
    import User from "../lib/User.svelte";

    let users = [
        {
        id:1,
        image:'src/assets/images/user1.png',
        name:'John',
        email:'john@flaticon.com',
        active:true,

    },
    {
        id:2,
        image:user2,
        name:'Ram',
        email:'ram@flaticon.com',
        active:false,

    },
    {
        id:3,
        image:user3,
        name:'Rockey',
        email:'rockey@flaticon.com',
        active:false,

    },

    ];
    const Getusers = () => {
        return users;
    };
  </script>
  
  <div>
    <h3 class="text-2xl text-center mt-10"> List of users</h3>
    {#each Getusers() as user, i (user.id)}
        <User {user} {i} />
    {:else}
        <p>No data found</p>
    {/each}
  </div>