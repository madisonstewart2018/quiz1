#this function uses the variables matrix and vector.
def matVec(matrix, vector):
  '''
  The function takes in a matrix with a vector, and for each element in one row multiplies by each number in the vector and     then adds them together. Function returns a new vector.
  '''
  new_x = []
  for i in range(len(matrix)):
    #i.e. in range(3) so (0, 1, 2)
    product = 0
    for j in range(len(vector)):
      #i.e. in range(3) so (0, 1, 2)
      product += matrix[i][j] * vector[j]
      #the product is then the prodcut (0) + matrix of i(outer range(3)) and j(inner range(3)) times the vector of j(outer            range(3)). The computer goes through and multiplies all of this together.
    new_x.append(product)
    #adds the prodcut found above to the end of new_x. So it puts the answer(product) in the brackets of new_x.
  return new_x

#this is the testing variables.
testmatrix01 = [[1, 2, 3], [3, 4, 5], [6, 7, 8]]
testmatrix02 = [1]
testmatrix03 = 'this is a test'

testvector01 = [1, 2, 3]
testvector02 = [[1, 2, 3], [3, 4, 5], [5, 6 ,7]]
testvector03 = 5

print(matVec(testmatrix01, testvector01))
#print(matVec(testmatrix02, testvector02))
#print(matVec(testmatrix03, testvector03))
