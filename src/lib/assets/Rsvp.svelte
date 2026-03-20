<script lang="ts">
let email = $state('');

function LetsRsvp() {
    let url = "https://forms.fillout.com/t/chsK1ZRiious?email=" + email;
    
    window.location.href = url;
}
</script>

<style>
    .container {
        display: flex;
        gap: 6px;
        align-items: center;
    }

    input {
        border-radius: 16px;
        padding: 12px 16px;
        font-size: clamp(16px, 3vw, 25px);
        width: clamp(200px, calc(100vw - 120px), 320px);
        border: 1px solid #ccc;
    }

    button {
        width: clamp(45px, 10vw, 55px);
        height: clamp(45px, 10vw, 55px);
        border-radius: 70%;
        background: white;
        border: 2px solid #333;
        font-size: clamp(18px, 2.5vw, 24px);
        cursor: pointer;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-shrink: 0;
        transition: all 0.3s ease-in-out;
    }

    @media (max-width: 480px) {
        .container {
            flex-direction: column;
            gap: 10px;
        }
        input {
            width: 100%;
        }
    }
    button:hover {
        transform: scale(1.08)
    }
</style>


<div class="container">
    <input bind:value={email} placeholder="you@hackclub.com">
    <button onclick={LetsRsvp}>→</button>
</div>