<template>
    <section id="meet-the-author">
      <h2>More About Damon Vaughn</h2>
      <p>Damon Vaughn is a professor of psychology at the University of Toronto, a clinical psychologist and the author of the multi-million copy bestseller “The story of my life.”</p>
      <button class="buttonMeetAuthor">Meet The Author</button>
    </section>
</template>

<script>
export default {
    name: "MeetTheAuthor"
}
</script>

<style lang="scss" scoped>

  @import '../styles/vars.scss';
  @import url('https://fonts.googleapis.com/css2?family=Kristi&display=swap');

  #meet-the-author {
    width: 70%;
    text-align: center;
    margin: 100px auto;

    h2 {
      font-family: "Kristi";
      color: $saffron;
      font-weight: lighter;
      font-size: 80px;
    }

    p {
      margin-top: 10px;
      font-size: 30px;
      line-height: 40px;
    }

    .buttonMeetAuthor {
      margin-top: 50px;
      background-color: $keppel;
      border: none;
      padding: 12px 35px;
      color: $white;
      border-radius: 5px;
      font-size: 18px;
      cursor: pointer;
      transition: 0.1s ease-out;

      &:hover {
        transition: 0.1s linear;
        background-color: $blueLagoon;
      }
    }
  }
</style>