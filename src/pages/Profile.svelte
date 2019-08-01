<script>
    import Nav from "../components/Nav.svelte";

    const navOptions = [
        {name: "Account Setting", url: "/profile/settings", position: ""},
        {name: "Linked Accoutns", url: "/profile/linked", position: ""},
        {name: "My Groups", url: "/profile/groups", position: ""}
    ];
</script>
<style>
.profile-header {
    height: 400px;
    position: relative;
}
.profile-image-wrapper {
    text-align: center;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
.profile-image {
    border-radius: 50%;
    height: 128px;
    width: 128px;
    text-align: center;
    display: inline-block;
}
.profile-header-text {
   
    text-align: center;
}
.profile-header-name {

    font-size: 32px;
    font-weight: 600;
}

</style>
<div class="profile">
	<div class="profile-header">
		<div class="profile-image-wrapper is-128x128">
			<img
				src="http://lorempixel.com/640/480/people"
				alt=""
				class="profile-image"
			/>
            <div class="profile-header-text profile-header-name">
			Donglin Wang
            </div>
             <div class="profile-header-text">
			Live Everyday
            </div>
		</div>	
	</div>
</div>

<Nav links={navOptions} linkFloat="middle"/>