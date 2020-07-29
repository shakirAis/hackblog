export default {
  async asyncData({ params, payload }) {
    if (payload) return { blogPost: payload };
    else
      return {
        blogPost: await require(`~/content/blog/${params.blog}.json`),
      };
  },
};
