<script>
    import IconButton from "$lib/components/ui/IconButton.svelte";
    const {title = ""} = $props();
</script>

<div class="newsletter">
    <IconButton src="/message-icon.png" alt="newsletter icon" size={48} />

    <div class="content">
        <div class="title">{title}</div>
        <div class="signup">Sign Up</div>
    </div>
</div>

<style>
    .newsletter {
        display: flex;
        align-items: center;
        gap: 16px;

        padding: 18px;
        border-radius: 16px;

        border: 1px solid rgba(255,255,255,0.08);
        background: rgba(255,255,255,0.02);

        cursor: pointer;
        transition: all 0.2s;
    }

    .newsletter:hover {
        background: rgba(255,255,255,0.05);
    }

    .title {
        font-weight: 600;
    }

    .signup {
        font-size: 14px;
        opacity: 0.7;
    }
</style>