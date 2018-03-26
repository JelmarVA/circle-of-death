<template>
  <div class="cd-modal" id="circleOfDeath">
    <div class="modal-content">
      <h2>My Modal Content</h2>
  
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ad modi repellendus, optio eveniet eligendi molestiae? Fugiat, temporibus! A rerum pariatur neque laborum earum, illum voluptatibus eum voluptatem fugiat, porro animi tempora? Sit harum nulla,
        nesciunt molestias, iusto aliquam aperiam est qui possimus reprehenderit ipsam ea aut assumenda inventore iste! Animi quaerat facere repudiandae earum quisquam accusamus tempora, delectus nesciunt, provident quae aliquam, voluptatum beatae quis
        similique in maiores repellat eligendi voluptas veniam optio illum vero! Eius, dignissimos esse eligendi veniam.
      </p>
  
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Debitis saepe amet sit fugit rerum, corporis minus vitae officia quaerat incidunt voluptate, blanditiis ea est quibusdam voluptas animi quasi totam magni, commodi praesentium. Possimus quam illo
        ipsam iste unde totam cupiditate deleniti, impedit assumenda hic eligendi natus tempora dolores quod mollitia ab non sunt eaque adipisci, suscipit quas aliquid officiis beatae. Necessitatibus voluptatibus, perferendis tenetur perspiciatis adipisci
        nesciunt eum ex fuga commodi iure numquam enim rem ullam labore nisi magni sint voluptatem quos! Eum iure exercitationem voluptates repellendus culpa doloremque laborum animi illum, sint fugit soluta possimus a fuga veritatis molestias corporis
        placeat illo pariatur dolor reiciendis earum, sapiente omnis. Placeat maiores omnis, porro officia, laborum eos. Fugiat mollitia inventore consequuntur odit eaque, rerum recusandae, eum sint molestiae consequatur culpa deserunt quae aliquid dolor
        tempora tenetur architecto repellendus enim quasi atque, odio voluptas. Tenetur repellendus explicabo ipsum inventore quia aut eos expedita necessitatibus asperiores blanditiis! Delectus nisi laudantium ipsum! Quasi blanditiis corrupti dicta maiores
        placeat laboriosam delectus ipsum facere voluptas, magnam voluptatibus, perferendis alias ullam saepe, perspiciatis recusandae voluptates, dolores praesentium?
      </p>
    </div>
  
    <a href="#0" class="modal-close">Close</a>
  </div>
</template>

<style>
  .cd-modal {
    position: fixed;
    top: 0;
    left: 0;
    z-index: 3;
    height: 100%;
    width: 100%;
    overflow: hidden;
    opacity: 0;
    visibility: hidden;
    background-color: #ef8692;
    -webkit-transition: opacity .3s 0s, visibility 0s .3s;
    transition: opacity .3s 0s, visibility 0s .3s;
  }
  
  .cd-modal .modal-content {
    height: 100%;
    overflow-y: auto;
    padding: 3em 5%;
  }
  
  .cd-modal h1,
  .cd-modal h2 {
    text-align: center;
  }
  
  .cd-modal p {
    line-height: 1.6;
    margin: 2em auto;
    max-width: 800px;
  }
  
  .cd-modal .modal-close {
    /* 'X' icon */
    position: absolute;
    z-index: 1;
    top: 20px;
    right: 5%;
    height: 45px;
    width: 45px;
    border-radius: 50%;
    overflow: hidden;
    white-space: nowrap;
    text-indent: 100%;
    color: transparent;
    visibility: hidden;
    opacity: 0;
    -webkit-transform: scale(0);
    transform: scale(0);
    -webkit-transition: visibility 0s .3s, opacity .3s 0s, -webkit-transform .3s 0s;
    transition: visibility 0s .3s, opacity .3s 0s, -webkit-transform .3s 0s;
    transition: transform .3s 0s, visibility 0s .3s, opacity .3s 0s;
    transition: transform .3s 0s, visibility 0s .3s, opacity .3s 0s, -webkit-transform .3s 0s;
  }
  
  .cd-modal .modal-close::before,
  .cd-modal .modal-close::after {
    content: '';
    display: inline-block;
    position: absolute;
    height: 2px;
    width: 20px;
    top: calc(50% - 1px);
    left: calc(50% - 10px);
  }
  
  .cd-modal .modal-close::before {
    -webkit-transform: rotate(45deg);
    transform: rotate(45deg);
  }
  
  .cd-modal .modal-close::after {
    -webkit-transform: rotate(-45deg);
    transform: rotate(-45deg);
  }
  
  .cd-modal.visible {
    opacity: 1;
    visibility: visible;
    -webkit-transition: opacity .7s, visibility 0s;
    transition: opacity .7s, visibility 0s;
  }
  
  .cd-modal.visible .modal-content {
    /* this fixes the buggy scrolling on webkit browsers - mobile devices only - when overflow property is applied */
    -webkit-overflow-scrolling: touch;
  }
  
  .cd-modal.visible .modal-close {
    visibility: visible;
    opacity: 1;
    -webkit-transition: visibility 0s 0s, opacity .3s 0s, -webkit-transform .3s 0s;
    transition: visibility 0s 0s, opacity .3s 0s, -webkit-transform .3s 0s;
    transition: transform .3s 0s, visibility 0s 0s, opacity .3s 0s;
    transition: transform .3s 0s, visibility 0s 0s, opacity .3s 0s, -webkit-transform .3s 0s;
    -webkit-transform: scale(1);
    transform: scale(1);
  }
  
  @media only screen and (min-width: 1100px) {
    .cd-modal .modal-content {
      padding: 6em 5%;
    }
    .cd-modal .modal-close {
      height: 60px;
      width: 60px;
    }
    .cd-modal .modal-close::before,
    .cd-modal .modal-close::after {
      height: 2px;
      width: 26px;
      top: calc(50% - 1px);
      left: calc(50% - 13px);
    }
    .cd-modal p {
      font-size: 2rem;
    }
  }
</style>

