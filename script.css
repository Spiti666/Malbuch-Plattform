document.addEventListener('DOMContentLoaded', () => {
    const blogLinks = document.querySelectorAll('.blog-post a');
    const modal = document.createElement('div');
    modal.id = 'blogModal';
    modal.style.display = 'none';
    modal.style.position = 'fixed';
    modal.style.top = '50%';
    modal.style.left = '50%';
    modal.style.transform = 'translate(-50%, -50%)';
    modal.style.backgroundColor = '#fff';
    modal.style.padding = '20px';
    modal.style.boxShadow = '0 0 10px rgba(0, 0, 0, 0.3)';
    modal.style.zIndex = '1001';
    modal.style.borderRadius = '10px';
    modal.style.maxWidth = '600px';
    modal.style.width = '90%';
    modal.innerHTML = `
        <h3 id="modalTitle"></h3>
        <p id="modalContent"></p>
        <button id="closeModal" style="margin-top: 15px; padding: 5px 10px; background-color: #ff6699; color: #fff; border: none; border-radius: 5px; cursor: pointer;">Schließen</button>
    `;

    document.body.appendChild(modal);

    const blogContents = {
        'Vorteile des Malens für die kindliche Entwicklung': 'Das Malen fördert nicht nur die Kreativität, sondern hilft auch bei der Entwicklung wichtiger motorischer Fähigkeiten. Kinder lernen, ihre Vorstellungskraft zu nutzen, Formen zu erkennen und Farben zu unterscheiden. Diese Aktivität unterstützt zudem die Konzentration und kann ein tolles Werkzeug zur Stressbewältigung sein. Das Malen ermöglicht es Kindern, sich auszudrücken und ihre Emotionen auf eine spielerische Art und Weise zu verarbeiten.',
        'Tipps für kreative Aktivitäten mit Kindern': 'Kreative Aktivitäten sind ein wunderbarer Weg, um Zeit mit Ihren Kindern zu verbringen und ihre Fantasie zu beflügeln. Versuchen Sie einfache Projekte wie das Basteln mit recycelten Materialien oder das Zeichnen mit verschiedenen Techniken wie Fingerfarben oder Wachsmalstiften. Ein gemeinsames Malprojekt kann nicht nur den Spaßfaktor erhöhen, sondern auch die Bindung stärken. Es ist erstaunlich, wie viel Freude ein einfaches kreatives Spiel bringen kann.',
        'DIY-Bastelprojekte für zu Hause': 'DIY-Bastelprojekte sind ideal, um regnerische Nachmittage zu Hause in spaßige Abenteuer zu verwandeln. Mit einfachen Materialien wie Papier, Schere, Farben und Kleber lassen sich kreative Kunstwerke schaffen. Eine Idee: Basteln Sie ein Pop-up-Buch, in dem jedes Familienmitglied eine Seite gestaltet. Solche Projekte regen die Fantasie an und geben Kindern ein Erfolgserlebnis, wenn sie ihr Werk stolz präsentieren können.'
    };

    blogLinks.forEach(link => {
        link.addEventListener('click', (event) => {
            event.preventDefault();
            const blogTitle = event.target.parentElement.querySelector('h3').textContent;

            document.getElementById('modalTitle').textContent = blogTitle;
            document.getElementById('modalContent').textContent = blogContents[blogTitle];
            modal.style.display = 'block';
        });
    });

    document.getElementById('closeModal').addEventListener('click', () => {
        modal.style.display = 'none';
    });

    // Header hide/show on scroll
    let lastScrollTop = 0;
    const header = document.getElementById('mainHeader');

    window.addEventListener('scroll', () => {
        let currentScroll = window.pageYOffset;
        if (currentScroll > lastScrollTop) {
            header.style.top = '-70px'; // Versteckt den Header beim Scrollen nach unten
            header.style.transition = 'top 0.5s ease-in-out'; // Sanfte Animation
        } else {
            header.style.top = '0'; // Zeigt den Header beim Scrollen nach oben
            header.style.transition = 'top 0.5s ease-in-out'; // Sanfte Animation
        }
        lastScrollTop = currentScroll <= 0 ? 0 : currentScroll; // Verhindert negatives Scrollen
    });
});
