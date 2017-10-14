<template>
  <section class="container">
  <nuxt-link to="Kunton">Kunton</nuxt-link>
    <div>
      <h1>Learn to PR</h1>
      <nuxt-link to="Sahphan">Sahaphan</nuxt-link> <br>
      <nuxt-link to="Rachata">Rachata</nuxt-link>
      <nuxt-link to="/sirirat">sirirat</nuxt-link>
      <nuxt-link to="warakana">About</nuxt-link>
      <nuxt-link to="Rittiphon">Rittiphon</nuxt-link>
      <nuxt-link to="/chonticha">chonticha</nuxt-link>
      <nuxt-link to="/Nat">Nat</nuxt-link>
    </div>

    <h1>MEAL EXPRESS!</h1>
    <div class="container"><p2>
      NAME : <input type="text" name="name" v-model="name"><br>
      ADDRESS : <input type="text" name="add" v-model="add"><br>
      TEL : <input type="text" name="tel" v-model="tel"><br>
    </p2></div><br>
    <div class="container">
      MEAL : <select>
                <option value="1">ข้าวไข่เจียว</option>
                <option value="2">ข้าวเหนียวหมูปิ้ง</option>
                <option value="3">ผัดมาม่า</option>
                <option value="4">ยำวุ้นเส้น</option>
              </select>

    </div><br>
                                <br>   <div class="col-md-12">
                                       <div class="form-group">
                                           <!-- Replace data-sitekey with your own one, generated at https://www.google.com/recaptcha/admin -->
                                           <div class="g-recaptcha" data-sitekey="6LfKURIUAAAAAO50vlwWZkyK_G2ywqE52NU7YO0S"></div>
                                       </div>
                                   </div>
                                   <br>
                                   <div class="col-md-12">
                                       <input type="submit" class="submit" value="submit" href="#">&nbsp;
                                       <input type="reset" class="reset" value="reset">
                                   </div>

                               </div>
                               <div class="row">
                               </div>
                           </div>

                       </form>

                   </div><!-- /.8 -->

               </div> <!-- /.row-->

           </div> <!-- /.container-->

           <script src="https://code.jquery.com/jquery-1.12.0.min.js"></script>
           <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js"></script>
           <script src='https://www.google.com/recaptcha/api.js'></script>
           <script src="validator.js"></script>
           <script src="contact.js"></script>

  </section>
</template>

<script>
export default {
  components: {
  }
}
</script>

<style>
</style>
