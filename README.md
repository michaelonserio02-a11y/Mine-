<script>
    function sayYes() {
        // Hide the question and buttons, show the happy message
        document.querySelector('h2').style.display = 'none';
        document.querySelector('#yesBtn').style.display = 'none';
        document.querySelector('#noBtn').style.display = 'none';
        document.querySelector('#loveMsg').style.display = 'block';
    }

    // Function to move the 'No' button randomly when hovered or clicked
    document.getElementById('noBtn').addEventListener('mouseover', function() {
        const noBtn = document.getElementById('noBtn');
        const container = document.querySelector('.card');

        // Calculate random positions within the card boundaries
        // Offsets added to ensure the whole button stays within the container
        const newX = Math.random() * (container.offsetWidth - noBtn.offsetWidth - 60) + 30; 
        const newY = Math.random() * (container.offsetHeight - noBtn.offsetHeight - 180) + 100;
        
        noBtn.style.position = 'absolute';
        noBtn.style.left = newX + 'px';
        noBtn.style.top = newY + 'px';
    });
</script>

