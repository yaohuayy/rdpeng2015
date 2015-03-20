# rdpeng2015
##This function creates a special "matrix" object that can cache its inverse.
makeCacheMatrix <- function(x = matrix(runif(n*n),n,n),id=1:Inf) {
  n <- id
  n <- as.integer(n)
  x<- matrix(runif(n*n),n,n)
  if(det(x)==0){
    return(x)
  }
  else{
    solve(x)
    return(solve(x))
  }
  return (solve(x))
}
