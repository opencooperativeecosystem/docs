# Current Architecture



![Current OCE architecture](https://blobscdn.gitbook.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-L9ditaV2urtKK1UEJuL%2F-L9k6Tot3ZaKk0lSryMe%2F-L9k7Qs4g7BEkduSDSWv%2FcurrentArchitecture.png?alt=media&token=dfbb201c-d613-49b8-a7b6-22cdcdce9754)

## Description {#description}

In the diagram, the rectangles inside the yellow ValueNetwork box are django apps within one django project. Mostly this reflects the Value Accounting app.

The Work App was created when NRP was forked to become OCP. It has some of the original NRP pages copied there, and improved, plus new features of integration with FairCoin, membership processes, etc. The Value Accounting App is the original NRP with a few upgrades, and being used as the "admin app" for admin people and when a function has not yet been moved to the work app.  


