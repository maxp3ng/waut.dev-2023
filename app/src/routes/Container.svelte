<div>
    // step 1, add a div with absolute position
    <div data-position="absolute">
        // step 2, add a second div inside the first div, also with absolute position;
        <div data-position="absolute">
            // step 3, animate the child div across the screen, moving it x pixels to the right every iteration
            <div data-x="1">
                <p> data </p>
                // this should scroll diagonally
            </div>
        </div>
    </div>
</div>

