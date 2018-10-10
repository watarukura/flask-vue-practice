<script>
// eslint-disable-next-line
import axios from 'axios';

export default {
  // eslint-disable-next-line
  name: 'Ping',
  data() {
    return {
      // eslint-disable-next-line
      msg: '',
    };
  },
  methods: {
    getMessage() {
      // eslint-disable-next-line
      const path = 'http://localhost:5000/ping';
      axios
        .get(path)
        // eslint-disable-next-line
        .then(res => {
          this.msg = res.data;
        })
        // eslint-disable-next-line
        .catch(error => {
          // eslint-disable-next-line
          console.errro(error);
        });
      // eslint-disable-next-line
    },
  },
  created() {
    this.getMessage();
    // eslint-disable-next-line
  },
};
</script>
