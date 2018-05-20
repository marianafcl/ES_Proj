Tanto a politica otimista, como a politica pessimista determinam como as transações acedem aos dados. 
Uma politica otimista significa que um registo especifico da tabela da base de dados está aberto para todas as sessões de utilizador ou transações. 
Portanto ao utilizar uma politica otimista não estamos a bloquear nenhum registo da base de dados. 
Logo é uma boa politica para ser utilizada quando estamos a fazer muitos reads. 
Como o fenixframework utiliza uma politica otimista, quando se corre os 100Reads a taxa de erro é perto de zero e é mais rápido na sua execução. 
No entanto, quando se corre o teste dos 30Writes verifica-se a existência de alguns erros, uma vez que não é garantida a integridade dos dados. 
Nos 100Writes, não ocorre nenhum erro porque não existe reads em simultâneo. 
