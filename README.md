<%@ Page language="c#" Inherits="UI.Abstracts.PageBase"%>
<script runat="server">
    protected override void Construct() {
        base.Construct();
        HasLayout = false;
    }

    void Page_Load(object sender, System.EventArgs e) {
        //<CODE_TAG_105653> Dav
        if (Request.QueryString["PSQ"].As<int>(1) == 2)
            Response.Redirect("/PSQuoter/modules/Quote/Workflow/QuoteWorkflow.aspx?RptType=2");
        //</CODE_TAG_105653> Dav
        // redirect to home page
        if(X.Web.WebContext.Current.Application.DefaultUrl != null)
            Response.Redirect(X.Web.WebContext.Current.Application.DefaultUrl );
        
        //<code_tag_01>
    }
</script>
