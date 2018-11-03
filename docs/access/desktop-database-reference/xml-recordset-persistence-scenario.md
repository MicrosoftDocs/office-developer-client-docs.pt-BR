---
title: Cenário de persistência do Recordset XML
TOCTitle: XML Recordset persistence scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4840b59f8f145b17b45a9732443d3f844b336868
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945485"
---
# <a name="xml-recordset-persistence-scenario"></a>Cenário de persistência do Recordset XML

**Aplica-se a**: Access 2013, o Office 2013

Neste cenário, você criará um aplicativo ASP (Active Server Pages) que salva o conteúdo de um objeto **Recordset** diretamente no objeto **Response** ASP.

> [!NOTE]
> [!OBSERVAçãO] Este cenário exige que seu servidor tenha o IIS 5.0 (Internet Information Server) ou posterior instalado.

O **Recordset** retornado é exibido no Internet Explorer usando um [RDS.DataControl](datacontrol-object-rds.md).

As seguintes etapas são necessárias para criar este cenário:

1.  Configurar o aplicativo.
2.  Obter os dados.
3.  Enviar os dados.
4.  Receber e exibir os dados.

## <a name="step-1-set-up-the-application"></a>Etapa 1: Configurar o aplicativo

1. Crie um diretório virtual do IIS chamado **XMLPersist** com permissões de script. 

2. Crie dois novos arquivos de texto na pasta para o qual os pontos do diretório virtual, um nomeado **XMLResponse.asp**e o outro chamado **Default. htm**.


## <a name="step-2-get-the-data"></a>Etapa 2: Obter os dados

Nesta etapa, você gravará o código para abrir um **Recordset** ADO e preparar para enviá-lo ao cliente. 

1. Abra o arquivo XMLResponse.asp com um editor de texto, como o Bloco de Notas do Windows, e insira o seguinte código:

   ```vb 
        
        <%@ language="VBScript" %> 
        
        <!-- #include file='adovbs.inc' --> 
        
        <% 
        Dim strSQL, strCon 
        Dim adoRec  
        Dim adoCon  
        Dim xmlDoc  
        
        ' You will need to change "slqServer" below to the name of the SQL  
        ' server machine to which you want to connect. 
        strCon = "Provider=sqloledb;Data Source=sqlServer;Initial Catalog=Pubs;Integrated Security=SSPI;" 
        Set adoCon = server.createObject("ADODB.Connection") 
        adoCon.Open strCon 
        
        strSQL = "SELECT Title, Price FROM Titles ORDER BY Price" 
        Set adoRec = Server.CreateObject("ADODB.Recordset") 
        adoRec.Open strSQL, adoCon, adOpenStatic, adLockOptimistic, adCmdText 
   ```

2. Certifique-se de alterar o valor do parâmetro fonte de dados em strCon com o nome do seu computador Microsoft SQL Server.

3. Mantenha o arquivo aberto e vá para a próxima etapa.

## <a name="step-3-send-the-data"></a>Etapa 3: Enviar os dados

Agora que você tem um **Recorset**, você precisa enviá-lo ao cliente, salvando-o como XML no objeto **Response** ASP. 

1. Adicione o seguinte código na parte inferior do XMLResponse.asp:

   ```vb 
    
    Response.ContentType = "text/xml" 
    Response.Expires = 0 
    Response.Buffer = False 
    
    
    Response.Write "<?xml version='1.0'?>" & vbNewLine 
    adoRec.save Response, adPersistXML 
    adoRec.Close 
    Set adoRec=Nothing 
    %> 
   ```

   Observe que o objeto de **resposta** do ASP é especificado como destino para o método **Recordset** [Salvar](save-method-ado.md) . O destino do método **Save** pode ser qualquer objeto que ofereça suporte à interface **IStream**, como um objeto [Stream](stream-object-ado.md) ADO ou um nome de arquivo que inclui o caminho completo no qual o **Recordset** deve ser salvo.

2. Salve e feche o arquivo XMLResponse.asp antes de ir para a próxima etapa. Também copiar o arquivo adovbs de c:\\Program Files\\arquivos comuns\\sistema\\pasta Ado na mesma pasta onde está o arquivo XMLResponse.asp.

## <a name="step-4-receive-and-display-the-data"></a>Etapa 4: Receber e exibir os dados

Nesta etapa, você criará um arquivo HTML com um [incorporado RDS. DataControl](datacontrol-object-rds.md) objeto apontando para o arquivo XMLResponse.asp para obter o **conjunto de registros**. 

1. Abra o default. htm com um editor de texto, como o bloco de notas do Windows e adicione o código a seguir. Substitua "sqlserver" no URL pelo nome do seu computador servidor.

   ```html 
    
    <HTML> 
    <HEAD><TITLE>ADO Recordset Persistence Sample</TITLE></HEAD> 
    <BODY> 
    
    <TABLE DATASRC="#RDC1" border="1"> 
    <TR> 
    <TD><SPAN DATAFLD="title"></SPAN></TD> 
    <TD><SPAN DATAFLD="price"></SPAN></TD> 
    </TR> 
    </TABLE> 

    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="RDC1"> 
    <PARAM NAME="URL" VALUE="XMLResponse.asp"> 
    </OBJECT> 
    
    </BODY> 
    </HTML> 
   ```

2. Feche o arquivo default.htm e salve-o na mesma pasta na qual você salvou o arquivo XMLResponse.asp. 

3. Usando o Internet Explorer 4.0 ou posterior, abra a URL `https://<sqlserver>/XMLPersist/default.htm` e observe os resultados. Os dados são exibidos em uma tabela DHTML vinculada. 

4. Agora, abra a URL `https://<sqlserver>/XMLPersist/XMLResponse.asp` e observe os resultados. O XML é exibido.




