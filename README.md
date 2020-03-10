# GrowthTeamAssignment
Assessment

###HERE's THE CODE JUST IN CASE YOU'RE UNABLE TO ACCESS THE FILE

SELECT DISTINCT category_id, product_id,

CASE 
	WHEN first_vote > second_vote then "First Product"
	WHEN second_vote> first_vote then "Second Product"
	else min(product_id)
	end as Winner
	
from Products

inner join Rounds on product_id=first_product 


group by product_id
order by category_id asc
