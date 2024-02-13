<script lang="ts">
    import FooterLogo from "$lib/assets/Company_Logo.png";
</script>

<footer
    class="relative w-full bottom-0 bg-crust grid max-lg:grid-rows-2 gap-3 lg:grid-cols-3 pt-6 max-lg:pb-6 lg:pb-0 lg:px-48 justify-evenly"
>
    <div class="max-lg:hidden lg:visible justify-self-start">
        <img src={FooterLogo} alt="logo" class="w-32 mb-1" />
        <p class="text-sm text-subtext1">© 2024</p>
    </div>

    <div class="justify-self-center">
        <h1 class="font-bold text-xl text-center mb-3">Contact</h1>
        <p>Max Rupp</p>
        <p>+1 (555) 555-5555</p>
        <p>5R6o0@example.com</p>
    </div>

    <div class="justify-self-end">
        <h1 class="font-bold text-xl text-center mb-3">Serviced Counties</h1>
        <div class="grid grid-cols-2 gap-10">
            <ul class="list-disc list-inside">
                <li>Anson</li>
                <li>Cabarrus</li>
                <li>Gaston</li>
                <li>Iredell</li>
            </ul>
            <ul class="list-disc list-inside">
                <li>Mecklenburg</li>
                <li>Rowan</li>
                <li>Stanly</li>
                <li>Union</li>
            </ul>
        </div>
    </div>
</footer>
