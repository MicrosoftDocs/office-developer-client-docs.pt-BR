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
# <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="db812-102">Cenário de persistência do Recordset XML</span><span class="sxs-lookup"><span data-stu-id="db812-102">XML Recordset persistence scenario</span></span>

<span data-ttu-id="db812-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="db812-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="db812-104">Neste cenário, você criará um aplicativo ASP (Active Server Pages) que salva o conteúdo de um objeto **Recordset** diretamente no objeto **Response** ASP.</span><span class="sxs-lookup"><span data-stu-id="db812-104">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a **Recordset** object directly to the ASP **Response** object.</span></span>

> [!NOTE]
> <span data-ttu-id="db812-105">[!OBSERVAçãO] Este cenário exige que seu servidor tenha o IIS 5.0 (Internet Information Server) ou posterior instalado.</span><span class="sxs-lookup"><span data-stu-id="db812-105">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</span></span>

<span data-ttu-id="db812-106">O **Recordset** retornado é exibido no Internet Explorer usando um [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="db812-106">The returned **Recordset** is displayed in Internet Explorer using an [RDS.DataControl](datacontrol-object-rds.md).</span></span>

<span data-ttu-id="db812-107">As seguintes etapas são necessárias para criar este cenário:</span><span class="sxs-lookup"><span data-stu-id="db812-107">The following steps are necessary to create this scenario:</span></span>

1.  <span data-ttu-id="db812-108">Configurar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="db812-108">Set up the application.</span></span>
2.  <span data-ttu-id="db812-109">Obter os dados.</span><span class="sxs-lookup"><span data-stu-id="db812-109">Get the data.</span></span>
3.  <span data-ttu-id="db812-110">Enviar os dados.</span><span class="sxs-lookup"><span data-stu-id="db812-110">Send the data.</span></span>
4.  <span data-ttu-id="db812-111">Receber e exibir os dados.</span><span class="sxs-lookup"><span data-stu-id="db812-111">Receive and display the data.</span></span>

## <a name="step-1-set-up-the-application"></a><span data-ttu-id="db812-112">Etapa 1: Configurar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="db812-112">Step 1: Set up the application</span></span>

1. <span data-ttu-id="db812-113">Crie um diretório virtual do IIS chamado **XMLPersist** com permissões de script.</span><span class="sxs-lookup"><span data-stu-id="db812-113">Create an IIS virtual directory named **XMLPersist** with script permissions.</span></span> 

2. <span data-ttu-id="db812-114">Crie dois novos arquivos de texto na pasta para o qual os pontos do diretório virtual, um nomeado **XMLResponse.asp**e o outro chamado **Default. htm**.</span><span class="sxs-lookup"><span data-stu-id="db812-114">Create two new text files in the folder to which the virtual directory points, one named **XMLResponse.asp**, and the other named **Default.htm**.</span></span>


## <a name="step-2-get-the-data"></a><span data-ttu-id="db812-115">Etapa 2: Obter os dados</span><span class="sxs-lookup"><span data-stu-id="db812-115">Step 2: Get the data</span></span>

<span data-ttu-id="db812-116">Nesta etapa, você gravará o código para abrir um **Recordset** ADO e preparar para enviá-lo ao cliente.</span><span class="sxs-lookup"><span data-stu-id="db812-116">In this step, you will write the code to open an ADO **Recordset** and prepare to send it to the client.</span></span> 

1. <span data-ttu-id="db812-117">Abra o arquivo XMLResponse.asp com um editor de texto, como o Bloco de Notas do Windows, e insira o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="db812-117">Open the file XMLResponse.asp with a text editor, such as Windows Notepad, and insert the following code:</span></span>

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

2. <span data-ttu-id="db812-118">Certifique-se de alterar o valor do parâmetro fonte de dados em strCon com o nome do seu computador Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="db812-118">Be sure to change the value of the Data Source parameter in strCon to the name of your Microsoft SQL Server computer.</span></span>

3. <span data-ttu-id="db812-119">Mantenha o arquivo aberto e vá para a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="db812-119">Keep the file open and go on to the next step.</span></span>

## <a name="step-3-send-the-data"></a><span data-ttu-id="db812-120">Etapa 3: Enviar os dados</span><span class="sxs-lookup"><span data-stu-id="db812-120">Step 3: Send the data</span></span>

<span data-ttu-id="db812-121">Agora que você tem um **Recorset**, você precisa enviá-lo ao cliente, salvando-o como XML no objeto **Response** ASP.</span><span class="sxs-lookup"><span data-stu-id="db812-121">Now that you have a **Recordset**, you need to send it to the client by saving it as XML to the ASP **Response** object.</span></span> 

1. <span data-ttu-id="db812-122">Adicione o seguinte código na parte inferior do XMLResponse.asp:</span><span class="sxs-lookup"><span data-stu-id="db812-122">Add the following code to the bottom of XMLResponse.asp:</span></span>

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

   <span data-ttu-id="db812-123">Observe que o objeto de **resposta** do ASP é especificado como destino para o método **Recordset** [Salvar](save-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="db812-123">Notice that the ASP **Response** object is specified as the destination for the **Recordset** [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="db812-124">O destino do método **Save** pode ser qualquer objeto que ofereça suporte à interface **IStream**, como um objeto [Stream](stream-object-ado.md) ADO ou um nome de arquivo que inclui o caminho completo no qual o **Recordset** deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="db812-124">The destination of the **Save** method can be any object that supports the **IStream** interface, such as an ADO [Stream](stream-object-ado.md) object, or a file name that includes the complete path to which the **Recordset** is to be saved.</span></span>

2. <span data-ttu-id="db812-125">Salve e feche o arquivo XMLResponse.asp antes de ir para a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="db812-125">Save and close XMLResponse.asp before going to the next step.</span></span> <span data-ttu-id="db812-126">Também copiar o arquivo adovbs de c:\\Program Files\\arquivos comuns\\sistema\\pasta Ado na mesma pasta onde está o arquivo XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="db812-126">Also copy the adovbs.inc file from C:\\Program Files\\Common Files\\System\\Ado folder to the same folder where you have the XMLResponse.asp file.</span></span>

## <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="db812-127">Etapa 4: Receber e exibir os dados</span><span class="sxs-lookup"><span data-stu-id="db812-127">Step 4: Receive and display the data</span></span>

<span data-ttu-id="db812-128">Nesta etapa, você criará um arquivo HTML com um [incorporado RDS. DataControl](datacontrol-object-rds.md) objeto apontando para o arquivo XMLResponse.asp para obter o **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="db812-128">In this step, you will create an HTML file with an embedded [RDS.DataControl](datacontrol-object-rds.md) object that points at the XMLResponse.asp file to get the **Recordset**.</span></span> 

1. <span data-ttu-id="db812-129">Abra o default. htm com um editor de texto, como o bloco de notas do Windows e adicione o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="db812-129">Open default.htm with a text editor, such as Windows Notepad, and add the following code.</span></span> <span data-ttu-id="db812-130">Substitua "sqlserver" no URL pelo nome do seu computador servidor.</span><span class="sxs-lookup"><span data-stu-id="db812-130">Replace "sqlserver" in the URL with the name of your server computer.</span></span>

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

2. <span data-ttu-id="db812-131">Feche o arquivo default.htm e salve-o na mesma pasta na qual você salvou o arquivo XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="db812-131">Close the default.htm file and save it to the same folder where you saved XMLResponse.asp.</span></span> 

3. <span data-ttu-id="db812-132">Usando o Internet Explorer 4.0 ou posterior, abra a URL `https://<sqlserver>/XMLPersist/default.htm` e observe os resultados.</span><span class="sxs-lookup"><span data-stu-id="db812-132">Using Internet Explorer 4.0 or later, open the URL `https://<sqlserver>/XMLPersist/default.htm` and observe the results.</span></span> <span data-ttu-id="db812-133">Os dados são exibidos em uma tabela DHTML vinculada.</span><span class="sxs-lookup"><span data-stu-id="db812-133">The data is displayed in a bound DHTML table.</span></span> 

4. <span data-ttu-id="db812-134">Agora, abra a URL `https://<sqlserver>/XMLPersist/XMLResponse.asp` e observe os resultados.</span><span class="sxs-lookup"><span data-stu-id="db812-134">Now open the URL `https://<sqlserver>/XMLPersist/XMLResponse.asp` and observe the results.</span></span> <span data-ttu-id="db812-135">O XML é exibido.</span><span class="sxs-lookup"><span data-stu-id="db812-135">The XML is displayed.</span></span>




