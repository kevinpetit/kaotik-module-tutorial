### Getting started!

Now, in order to get started we'll need our module that we built in the last chapters - we're going to continue where we left off. If you're unfamiliar with JavaScript, this section might be hard - a small lookup of some JavaScript\/jQuery modules can do wonders here!

Now, what's AJAX again? AJAX is a technology, basicly JavaScript, that allows you to update pieces of your webpage without having to do a full reload of our page. Imagine that you've got a site where you're showing the current score of a football match - on a normal site, you would need to refresh the page in order to modify the score. With AJAX, you can fetch the scores and update it without having to reload the entire page! In this example, our page would also need to reload every few minutes as we can't see when a goal has been made - we're guessing this. With AJAX, we can check this constantly \(for example every 30 seconds\), and our user won't even notice this!

This example really shows how powerful AJAX can be - so let's get started!

Let's open up our **templates\/people\_form.html **file and let's get started with editing. First, we should add jQuery to our page, however, if you're using an xBootstrap based theme, it will already be loaded! Don't load jQuery twice, as this can slow up your page and break your scripts.

```
<form class="form" name="people_form" method="post" id="people_form" action="index.php">    
    <fieldset class="form-group">
        <div class="form-group">        
            <label for="name"><{$smarty.const.PP_NAME}></label>        
            <input type="text" class="form-control" name="name" placeholder="<{$smarty.const.PP_NAME}>">    
        </div>    
        <div class="form-group">        
            <label for="name"><{$smarty.const.PP_ADDRESS}></label>        
            <input type="text" class="form-control" name="address" placeholder="<{$smarty.const.PP_ADDRESS}>">    
        </div> 
       <div class="form-group">   
             <label for="name"><{$smarty.const.PP_TELEPHONE}></label>        
             <input type="text" class="form-control" name="telephone" placeholder="<{$smarty.const.PP_TELEPHONE}>">    
        </div>    
        <div class="form-group">        
            <label for="name"><{$smarty.const.PP_EMAIL}></label>        
            <input type="text" class="form-control" name="email" placeholder="<{$smarty.const.PP_EMAIL}>">    
        </div>    
        <button class="btn btn-default" type="submit" name="listAll" value="List All">List all inputs</button>    
        <button class="btn btn-success" type="submit" name="submit" value="submit">Submit</button>    
    </fieldset>
</form>
<script>    
    $(document).ready(function()    
    {        
        $("#people_form").submit(function(e)        
        {            
            e.preventDefault();            
            alert('You clicked submit!');        
        });    
    });
</script>
```

I'll go over what we've changed:

* In the first line, we've added **id="people\_form". Don't forget to add this, or this won't work!**

* On the top of our form, we added a new block of code:



* Let's go over with what this does:


