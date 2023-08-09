<template>
  <div>
    <button
      type="button"
      class="contact-btn"
      data-bs-toggle="modal"
      data-bs-target="#exampleModal"
    >
      Contact Us
    </button>

    <!-- Modal -->
    <div
      class="modal fade"
      id="exampleModal"
      tabindex="-1"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <span
              type="button"
              class="close-btn"
              data-bs-dismiss="modal"
              aria-label="Close"
            >
              <span></span>
              <span></span>
            </span>
            <h1 class="modal-title fs-5" id="exampleModalLabel">Contact Us</h1>
          </div>
          <div class="modal-body">
            <form action="">
              <div class="form-floating mb-3">
                <input
                  type="email"
                  class="form-control"
                  id="floatingInput"
                  placeholder="name@example.com"
                />
                <label for="floatingInput">Email address</label>
              </div>
              <div class="form-floating">
                <textarea
                  class="form-control"
                  placeholder="Leave a comment here"
                  id="floatingTextarea2"
                  style="height: 100px"
                ></textarea>
                <label for="floatingTextarea2">Comments</label>
              </div>
              <button type="submit" class="btn-submit mt-3">
                Send Message
              </button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.modal {
  .modal-content {
    padding: 32px 28px 80px;
    background-color: var(--background-color);
    .modal-header,
    .modal-body,
    .modal-footer {
      border: none;
    }

    .modal-header {
      flex-direction: column;

      .close-btn {
        display: block;
        width: 24px;
        height: 24px;
        align-self: flex-end;
        span {
          width: 100%;
          height: 3px;
          background-color: var(--text-light);
          display: block;
          border-radius: 30px;
          transform: rotate(45deg) translate(3px, 3.5px);
          &:nth-child(2) {
            transform: rotate(-45deg) translate(-1px, 0.5px);
          }
        }
      }
      .modal-title {
        color: var(--text-light);
        margin-top: 24px;
        text-align: left;
        align-self: flex-start;
        font-family: var(--font-primary);
        font-size: 32px;
        font-weight: 700;
        line-height: 41px;
        letter-spacing: 0em;
      }
    }

    .modal-body {
      input,
      textarea,
      input:focus,
      textarea:focus {
        background: transparent;
        border: 1px solid #262661;
        outline: none;
        box-shadow: none;
      }
      label {
        color: var(--text-light);
        font-family: Poppins;
        font-size: 16px;
        font-weight: 400;
        line-height: 24px;
        background-color: transparent !important;
      }
      label::after {
        content: "";
        background-color: transparent !important;
      }
      .btn-submit {
        background-color: #262661;
        padding: 16px 24px 16px 24px;
        border-radius: 8px;
        font-family: Poppins;
        font-size: 16px;
        font-weight: 400;
        line-height: 24px;
        text-align: center;
        color: var(--text-light);
        border: none;
        width: 100%;
        margin-top: 32px !important;
      }
    }
  }
}

.contact-btn {
  display: flex;
  border: 1px solid var(--text-light);
  background-color: transparent;
  padding: 8px 16px;
  border-radius: 8px;
  color: var(--text-light);
  font-family: Poppins;
  font-size: 16px;
  font-weight: 400;
  line-height: 24px;
  letter-spacing: 0em;
  text-align: center;
  @media (max-width: 768px) {
    border-color: var(--background-color);
    color: var(--background-color);
    width: 90%;
    margin: 0 auto;
    justify-content: center;
  }
}
</style>