# LABORATÓRIO 

# Introducao-AmazonSimpleStorageService-S3  

![image](https://github.com/SamiraCavalcanti/Introducao-AmazonSimpleStorageService-S3-/assets/86758007/99a6a9a2-6cb1-4933-a160-5737258e41e7)







# OBJETIVOS    
Depois de concluir este laboratório, você saberá:

 Criar um bucket no Amazon S3      
 Adicionar um objeto a um bucket      
 Gerenciar permissões de acesso em um objeto e um bucket      
 Criar uma política de bucket      
 Usar versionamento de bucket      

# Como funciona     
O Amazon Simple Storage Service (Amazon S3) é um serviço de armazenamento de objetos que oferece escalabilidade, disponibilidade de dados, segurança e performance líderes do setor. Clientes de todos os portes e setores podem armazenar e proteger qualquer quantidade de dados de praticamente qualquer caso de uso, como data lakes, aplicações nativas da nuvem e aplicações móveis. Com classes de armazenamento econômicas e recursos de gerenciamento fáceis de usar, você pode otimizar custos, organizar dados e configurar controles de acesso ajustados para atender a requisitos específicos de negócios, organizacionais e de conformidade.      

# CENÁRIO DO LABORATÓRIO
Você trabalha para uma empresa que usa o Amazon S3 para o armazenamento de dados. Um aplicativo que fica em uma instância do EC2 precisa enviar dados de relatório para um bucket do S3 diariamente. Sua tarefa é criar um bucket do S3, que sua empresa usará para armazenar os dados de relatório. Para uma implantação bem-sucedida, a instância do EC2 deve ter privilégios suficientes para fazer upload e recuperar dados do bucket do S3. Por motivos de segurança, somente a instância do EC2 pode gravar dados no bucket do S3. Os arquivos do bucket do S3 também devem ser protegidos contra exclusão acidental. Este laboratório complementa o curso digital Getting Started with Amazon S3.   

# Tarefa 1: criar um bucket

Bucket com o nome reportbucket19861957 criado

![image](https://github.com/SamiraCavalcanti/Introducao-AmazonSimpleStorageService-S3-/assets/86758007/d3950007-2e9c-43c9-8839-929c3b4f986e)        


# Tarefa 2: fazer upload de um objeto no bucket
** Um objeto pode ser qualquer tipo de arquivo: um arquivo de texto, uma foto, um vídeo, um arquivo Zip etc. Ao adicionar um objeto ao Amazon S3, você tem a opção de incluir metadados personalizados com o objeto e definir permissões para controlar o acesso a ele.

Upload da captura de tela de um relatório

![image](https://github.com/SamiraCavalcanti/Introducao-AmazonSimpleStorageService-S3-/assets/86758007/89a2abb6-9e51-4d2c-98ea-7b828fe72dd8)



# Tarefa 3: tornar um objeto público

** Por questões de segurança  o objeto  é privado por padrão.

![image](https://github.com/SamiraCavalcanti/Introducao-AmazonSimpleStorageService-S3-/assets/86758007/0cc8870d-a663-441b-9839-7c984abbcfc0)    


Depois de efetuar as permissões necessárias, concedi acesso de leitura somente a esse objeto

![image](https://github.com/SamiraCavalcanti/Introducao-AmazonSimpleStorageService-S3-/assets/86758007/de28e8b5-cfc6-4d5e-9bcb-2feb05e955a0)

# Tarefa 4: testar a conectividade da instância do 

Testes realizados

** A saída indica o erro upload failed (falha de upload).         
Isso ocorre porque temos direitos de somente leitura para o bucket e não temos as permissões para executar a operação PutObject.

![image](https://github.com/SamiraCavalcanti/Introducao-AmazonSimpleStorageService-S3-/assets/86758007/55b2b19e-e6cb-4793-a417-cbc55d72d1ee)      

# Tarefa 5: criar uma política de bucket
**Uma política de bucket é um conjunto de permissões associadas a um bucket do S3. Ela pode ser usada para controlar         
o acesso a um bucket inteiro ou a diretórios específicos dentro de um bucket.

Politica criada e o upload foi feito com sucesso do arquivo (PutObject) da instância do EC2 para o bucket do S3.

![image](https://github.com/SamiraCavalcanti/Introducao-AmazonSimpleStorageService-S3-/assets/86758007/4dcd4f1b-853d-4dab-b03f-df5f774cee70)


![image](https://github.com/SamiraCavalcanti/Introducao-AmazonSimpleStorageService-S3-/assets/86758007/a4792aea-4bdf-4925-a274-d2283853ef17)      

 Recuperando um arquivo (GetObject) do S3 para a instância do EC2.

![image](https://github.com/SamiraCavalcanti/Introducao-AmazonSimpleStorageService-S3-/assets/86758007/50326517-2cee-4dc3-90d3-cf6bb0000ac3)

# Tarefa 6: explorar o versionamento
**O versionamento é um meio de manter diversas variantes de um objeto no mesmo bucket.          
Ele pode ser usado para preservação, recuperação e restauração de todas as versões de cada objeto armazenado no bucket do Amazon S3.       
Com o versionamento, você pode se recuperar facilmente de ações não intencionais do usuário e de falhas do aplicativo.

Versionamento habilitado 

![image](https://github.com/SamiraCavalcanti/Introducao-AmazonSimpleStorageService-S3-/assets/86758007/790771d3-b75c-4bcb-b410-c0380e13538d)




Nova versão do objeto editado  no bucket 

![image](https://github.com/SamiraCavalcanti/Introducao-AmazonSimpleStorageService-S3-/assets/86758007/35368382-00cb-44fa-8570-ae8fa7894cef)



Arquivo com texto inicial 

![image](https://github.com/SamiraCavalcanti/Introducao-AmazonSimpleStorageService-S3-/assets/86758007/51a791d7-0748-40e6-a155-956a9a23eba1)




Mesmo aquivo, porém foi acrescentado mais texto.

![image](https://github.com/SamiraCavalcanti/Introducao-AmazonSimpleStorageService-S3-/assets/86758007/cce1af35-4418-4b82-855d-76a5cf132e42)



























