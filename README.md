# R-Programming
# Coursera - R Programming 

# Week 3 Assignment 2


C:\Users\20292\Desktop\R Course Files


https://github.com/leigh-math/ProgrammingAssignment2.git


https://github.com/leigh-math/ProgrammingAssignment2.git


## Put comments here that give an overall description of what your
## functions do


## R Programming - Week 3 - Assignment 1        Feb 2016
## Leigh Matthews

########################################################################################

## makeCacheMatrix: This function creates a special "matrix" object.  We use it later solve for the inverse.


## This creates default for cacheSolve

makeCacheMatrix <- function(x = matrix()) {
	## Set default values (initialize)
	m <- NULL
	y <- NULL
	set <- function(y){
		x <<- y  ## caches the matrix
		m <<- NULL ## set a default
		}

pullin <- function(x)
solve_matrix <- function(solve) m <<- solve
my_matrix <- function() m

### Spit out the cache matrix
list(set = set, pullin = pullin, solve_matrix = solve_matrix, my_matrix = my_matrix)
}

########################################################################################

## cacheSolve: This function computes the inverse of the special "matrix" returned by 
## makeCacheMatrix above. If the inverse has already been calculated (and the matrix has not changed), 
## then the cachesolve should retrieve the inverse from the cache.

cacheSolve <- function(x=matrix(), ...) {
        ## Return a matrix that is the inverse of 'x'

	m <- x$my_matrix()
	if(!is.null(m)){
		message("Pulling in the Cached Matrix")
		return(m)
	}
	
	
	matrix <- x$pullin	  #Get the matrix
	m <- solve(matrix, ... )  #Get the inverse
	x$setmatrix(m)
	m				  #Output the result

}



#### Run cacheSolve with valid arguments. 




04416d0177860395272319ab90c435eea4884599
