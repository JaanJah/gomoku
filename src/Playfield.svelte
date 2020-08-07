<script lang="ts">
    const boxSize = 50;
    const fieldSize = 12;
    const marginFromField = 100;
    const offset = 25;
    export function createPlayfield() {
        const playfield = document.getElementById('playfield');
        for (let x = 0; x < fieldSize; x++) {
            for (let y = 0; y < fieldSize; y++) {
                const box = document.createElement('div');
                box.classList.add('box');
                box.classList.add('box_col' + y);
                box.classList.add('box_row' + x);

                box.style.marginTop = marginFromField + 'px';
                box.style.marginLeft = marginFromField + 'px';

                box.style.borderStyle = 'solid';
                box.style.borderWidth = '1px';
                box.style.top = x * boxSize + 'px';
                box.style.left = y * boxSize + 'px';
                box.style.width = '49px';
                box.style.height = '49px';
                box.style.position = 'absolute';
                playfield.appendChild(box);
            }
        }
    }

    export function createClickableDOM() {
        const playfield = document.getElementById('playfieldDOM');
        for (let x = 0; x < fieldSize + 1; x++) {
            for (let y = 0; y < fieldSize + 1; y++) {
                const box = document.createElement('div');
                box.classList.add('boxDOM');
                box.classList.add('box_col' + y);
                box.classList.add('box_row' + x);

                box.style.marginTop = marginFromField - offset + 'px';
                box.style.marginLeft = marginFromField - offset + 'px';

                box.style.borderStyle = 'solid';
                box.style.borderWidth = '1px';
                box.style.borderColor = 'red';
                box.style.borderRadius = '50%';
                box.style.top = x * boxSize + 'px';
                box.style.left = y * boxSize + 'px';
                box.style.width = '49px';
                box.style.height = '49px';
                box.style.position = 'absolute';
                playfield.appendChild(box);
            }
        }
    }

    // TODO:
    export function makeMove(box_col, box_row) {

    }
</script>
<div id="playfield"></div>
<div id="playfieldDOM"></div>