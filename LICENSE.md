makeCacheMatrix <- function(x = matrix()) {
  m<-NULL
  set<-function(y){
  x<<-y
  m<<-NULL
}
get<-function() x
setmatrix<-function(solve) m<<- solve
getmatrix<-function() m
list(set=set, get=get,
   setmatrix=setmatrix,
   getmatrix=getmatrix)
}

cacheSolve <- function(x=matrix(), ...) {
    m<-x$getmatrix()
    if(!is.null(m)){
      message("getting cached data")
      return(m)
    }
    datos<-x$get()
    m<-solve(datos, ...)
    x$setmatrix(m)
    m
}

## Put comments here that give an overall description of what your
## functions do

## Write a short comment describing this function

x<- makevector(c(1,2,3,4,...))


makeCacheMatrix <- function(x = matrix()) {
    
}


## Write a short comment describing this function

cacheSolve <- function(x, ...) {
    ## Return a matrix that is the inverse of 'x'
}







set<-makevector(c(1,2,3,...))
set$get()
## this function is to find get of the matrix

setmatrix<- makevector(c(1,2,3,...))  m<<-solve
set$setmatrix()
## this function is to find set of matrix

getmatrix<- makevector(c(1,2,3,...)) m
set$getmatrix()
## this function is to find getmatrix


inv<-makeCachematrix(m)
CacheSolve(inv)
## this is to find the cache of the matrix
## it also finds the inverse of the matrix
