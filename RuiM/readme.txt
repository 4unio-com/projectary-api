estrutura de pastas dentro da pasta go 
(workspace criado por defeito na %userprofile% mas pode ser alterado na PATH)
src -> pastas com as sources. Qualquer excutavel ter� a funcao main().
	   Tambem aqui s�o guardadas as dependencias sacadas com o go get <dependencia>
pkg -> pastas com as dependencias compiladas. Estas s�o necessarias depois de compilada a aplica��o
       .As dependencias em go s�o compiladas para ficheiros com o mesmo nome mas de extens�o .a
bin -> aqui ficam os executaveis das aplica��es compiladas.

* ao executar o comando go install <pasta_da_source> o compilador encarrega-se de compilar as dependecias e
  rotina principal e coloc�-las nas respectivas pastas pkg e bin.
  