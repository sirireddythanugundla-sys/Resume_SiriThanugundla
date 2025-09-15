var menu = document.querySelectorAll('#nav-list li a');

for(let i=0 ;i<menu.length;i++)
{
    menu[i].addEventListener('click',function(event){

        event.preventDefault();
        // var target = menu[i].innerHTML.trim().toLowerCase();
        var target=document.getElementById(this.innerHTML.trim().toLowerCase())
        console.log(target);
        var len=target.getBoundingClientRect().top;
        console.log(len);
    
        var scroll= setInterval(function()
        {
            window.scrollBy(0,20);
            if(window.pageYOffset+102>=len)
            {
                clearInterval(scroll);
            }
        },10)

    });
}
var skills= document.querySelectorAll('.skill-indicator >div');
var slide = setInterval(function()
{
    if(window.pageYOffset >= 406)
    {
    for(let i=0 ;i<skills.length;i++){
        
        let ani = skills[i];
        ani.style.width='0%'; 
        console.log(ani.style.width);



        let slide2=setInterval(function()
        {
            let x= parseInt(ani.style.width.substring(0,ani.style.width.length -1))
            ani.style.width = eval('x + 5') + '%';
            if(parseInt(ani.style.width.substring(0,ani.style.width.length -1)) >= ani.getAttribute('data-value'))
            {
                clearInterval(slide2);
            }

        },10)
    }
        clearInterval(slide);
    }
},100)

//percentagescrolled

var percentage= document.getElementById('percentage');

var bodyHeight = document.body.offsetHeight - window.innerHeight;


document.addEventListener('scroll',function()
{
    var presentheight = window.pageYOffset;
    percentage.innerHTML = Math.ceil(((presentheight)/bodyHeight)*100) +'%';
})
