Programmer name: Luis Rodriguez
Program purpose: To make a web app that showcases different books from vice city Miami
Program start: 25 10 2022 1115
Program end:
Last edited: 11/1/2022


25 10 2022 1120

Starting project beginning with the set up



25 10 2022 1134

configuring my project adding name: LuisBookStore
adding location: into my desktop
solution name will be the same as my project name


25 10 2022 1147
anabling razore runtime and checking off individual accounts
creating project after checking off individual accounts and choosing asp.net core web app (mvc)
project is finally being created.

25 10 2022 1156

commenting out the ssl in the json file under properties
following the tutorial, looking at the controllers , models, and views.

25 10 2022 1210

taking out the context in the parenthesis () in identity user under startup.cs



26 10 2022 1503


adding

// This method gets called by the runtime. Use this method to configure the HTTP request pipeline.

public void Configure(IApplicationBuilder app, IWebHostEnvironment env)

{

if (env.IsDevelopment())

{

app.UseDeveloperExceptionPage();

app.UseMigrationsEndPoint();

}

else

{

app.UseExceptionHandler("/Home/Error");

// The default HSTS value is 30 days. You may want to change this for production scenarios, see https://aka.ms/aspnetcore-hsts.

app.UseHsts();

}

app.UseHttpsRedirection();

app.UseStaticFiles();

app.UseRouting();

app.UseAuthentication();

app.UseAuthorization();

app.UseEndpoints(endpoints =>

{

endpoints.MapControllerRoute(

name: "default",

pattern: "{controller=Home}/{action=Index}/{id?}");

endpoints.MapRazorPages();

});

}


26 10 2022  1603

replacing things in the start up file.

Using quartz for my bootstrap

https://getbootstrap.com/docs/4.0/components/navbar/