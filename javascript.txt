document.addEventListener('DOMContentLoaded', () => {
    const categories = document.querySelectorAll('nav ul li a');
    
    categories.forEach(category => {
        category.addEventListener('click', function(e) {
            e.preventDefault();
            const targetSection = document.querySelector(this.getAttribute('href'));
            window.scrollTo({
                top: targetSection.offsetTop - 50,
                behavior: 'smooth'
            });
        });
    });
});
