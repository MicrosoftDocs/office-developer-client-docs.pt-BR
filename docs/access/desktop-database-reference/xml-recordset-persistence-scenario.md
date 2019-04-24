---
title: Cenário de persistência do conjunto de registros do XML
TOCTitle: XML Recordset persistence scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5bae48f3e9b2b5c3967b955c41ba01c634546164
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302588"
---
# <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="a19d7-102">Cenário de persistência do conjunto de registros do XML</span><span class="sxs-lookup"><span data-stu-id="a19d7-102">XML Recordset persistence scenario</span></span>

<span data-ttu-id="a19d7-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a19d7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a19d7-104">Neste cenário, você criará um aplicativo ASP (Active Server Pages) que salva o conteúdo de um objeto **Recordset** diretamente no objeto **Response** ASP.</span><span class="sxs-lookup"><span data-stu-id="a19d7-104">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a **Recordset** object directly to the ASP **Response** object.</span></span>

> [!NOTE]
> <span data-ttu-id="a19d7-105">[!OBSERVAçãO] Este cenário exige que seu servidor tenha o IIS 5.0 (Internet Information Server) ou posterior instalado.</span><span class="sxs-lookup"><span data-stu-id="a19d7-105">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</span></span>

<span data-ttu-id="a19d7-106">O **Recordset** retornado é exibido no Internet Explorer usando um [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="a19d7-106">The returned **Recordset** is displayed in Internet Explorer using an [RDS.DataControl](datacontrol-object-rds.md).</span></span>

<span data-ttu-id="a19d7-107">As seguintes etapas são necessárias para criar este cenário:</span><span class="sxs-lookup"><span data-stu-id="a19d7-107">The following steps are necessary to create this scenario:</span></span>

1.  <span data-ttu-id="a19d7-108">Configurar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a19d7-108">Set up the application.</span></span>
2.  <span data-ttu-id="a19d7-109">Obter os dados.</span><span class="sxs-lookup"><span data-stu-id="a19d7-109">Get the data.</span></span>
3.  <span data-ttu-id="a19d7-110">Enviar os dados.</span><span class="sxs-lookup"><span data-stu-id="a19d7-110">Send the data.</span></span>
4.  <span data-ttu-id="a19d7-111">Receber e exibir os dados.</span><span class="sxs-lookup"><span data-stu-id="a19d7-111">Receive and display the data.</span></span>

## <a name="step-1-set-up-the-application"></a><span data-ttu-id="a19d7-112">Etapa 1: configurar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="a19d7-112">Step 1: Set up the application</span></span>

1. <span data-ttu-id="a19d7-113">Crie um diretório virtual do IIS \*\*\*\* chamado xmlpersist com permissões de script.</span><span class="sxs-lookup"><span data-stu-id="a19d7-113">Create an IIS virtual directory named **XMLPersist** with script permissions.</span></span> 

2. <span data-ttu-id="a19d7-114">Crie dois novos arquivos de texto na pasta para a qual o diretório virtual aponta, um chamado **xmlresponse. asp**e o outro chamado **Default. htm**.</span><span class="sxs-lookup"><span data-stu-id="a19d7-114">Create two new text files in the folder to which the virtual directory points, one named **XMLResponse.asp**, and the other named **Default.htm**.</span></span>


## <a name="step-2-get-the-data"></a><span data-ttu-id="a19d7-115">Etapa 2: obter os dados</span><span class="sxs-lookup"><span data-stu-id="a19d7-115">Step 2: Get the data</span></span>

<span data-ttu-id="a19d7-116">Nesta etapa, você gravará o código para abrir um **Recordset** ADO e preparar para enviá-lo ao cliente.</span><span class="sxs-lookup"><span data-stu-id="a19d7-116">In this step, you will write the code to open an ADO **Recordset** and prepare to send it to the client.</span></span> 

1. <span data-ttu-id="a19d7-117">Abra o arquivo XMLResponse.asp com um editor de texto, como o Bloco de Notas do Windows, e insira o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="a19d7-117">Open the file XMLResponse.asp with a text editor, such as Windows Notepad, and insert the following code:</span></span>

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

2. <span data-ttu-id="a19d7-118">Certifique-se de alterar o valor do parâmetro da fonte de dados no strCon para o nome do computador do Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a19d7-118">Be sure to change the value of the Data Source parameter in strCon to the name of your Microsoft SQL Server computer.</span></span>

3. <span data-ttu-id="a19d7-119">Mantenha o arquivo aberto e vá para a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="a19d7-119">Keep the file open and go on to the next step.</span></span>

## <a name="step-3-send-the-data"></a><span data-ttu-id="a19d7-120">Etapa 3: enviar os dados</span><span class="sxs-lookup"><span data-stu-id="a19d7-120">Step 3: Send the data</span></span>

<span data-ttu-id="a19d7-121">Agora que você tem um **Recorset**, você precisa enviá-lo ao cliente, salvando-o como XML no objeto **Response** ASP.</span><span class="sxs-lookup"><span data-stu-id="a19d7-121">Now that you have a **Recordset**, you need to send it to the client by saving it as XML to the ASP **Response** object.</span></span> 

1. <span data-ttu-id="a19d7-122">Adicione o seguinte código na parte inferior do XMLResponse.asp:</span><span class="sxs-lookup"><span data-stu-id="a19d7-122">Add the following code to the bottom of XMLResponse.asp:</span></span>

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

   <span data-ttu-id="a19d7-123">Observe que o objeto de **resposta** do ASP é especificado como o destino para o método [Save](save-method-ado.md) do **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="a19d7-123">Notice that the ASP **Response** object is specified as the destination for the **Recordset** [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="a19d7-124">O destino do método **Save** pode ser qualquer objeto que ofereça suporte à interface **IStream**, como um objeto [Stream](stream-object-ado.md) ADO ou um nome de arquivo que inclui o caminho completo no qual o **Recordset** deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="a19d7-124">The destination of the **Save** method can be any object that supports the **IStream** interface, such as an ADO [Stream](stream-object-ado.md) object, or a file name that includes the complete path to which the **Recordset** is to be saved.</span></span>

2. <span data-ttu-id="a19d7-125">Salve e feche o arquivo XMLResponse.asp antes de ir para a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="a19d7-125">Save and close XMLResponse.asp before going to the next step.</span></span> <span data-ttu-id="a19d7-126">Além disso, copie o arquivo adovbs. Inc da\\pasta C\\: arquivos\\de\\programas comuns do sistema de arquivos comum para a mesma pasta em que você tem o arquivo xmlresponse. ASP.</span><span class="sxs-lookup"><span data-stu-id="a19d7-126">Also copy the adovbs.inc file from C:\\Program Files\\Common Files\\System\\Ado folder to the same folder where you have the XMLResponse.asp file.</span></span>

## <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="a19d7-127">Etapa 4: receber e exibir os dados</span><span class="sxs-lookup"><span data-stu-id="a19d7-127">Step 4: Receive and display the data</span></span>

<span data-ttu-id="a19d7-128">Nesta etapa, você criará um arquivo HTML com um RDS incorporado [. ](datacontrol-object-rds.md)Objeto DataControl que aponta o arquivo xmlresponse. asp para obter o **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a19d7-128">In this step, you will create an HTML file with an embedded [RDS.DataControl](datacontrol-object-rds.md) object that points at the XMLResponse.asp file to get the **Recordset**.</span></span> 

1. <span data-ttu-id="a19d7-129">Abra o default. htm com um editor de texto, como o bloco de notas do Windows, e adicione o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a19d7-129">Open default.htm with a text editor, such as Windows Notepad, and add the following code.</span></span> <span data-ttu-id="a19d7-130">Substitua "sqlserver" no URL pelo nome do seu computador servidor.</span><span class="sxs-lookup"><span data-stu-id="a19d7-130">Replace "sqlserver" in the URL with the name of your server computer.</span></span>

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

2. <span data-ttu-id="a19d7-131">Feche o arquivo default.htm e salve-o na mesma pasta na qual você salvou o arquivo XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="a19d7-131">Close the default.htm file and save it to the same folder where you saved XMLResponse.asp.</span></span> 

3. <span data-ttu-id="a19d7-132">Usando o Internet Explorer 4,0 ou posterior, abra a `https://<sqlserver>/XMLPersist/default.htm` URL e observe os resultados.</span><span class="sxs-lookup"><span data-stu-id="a19d7-132">Using Internet Explorer 4.0 or later, open the URL `https://<sqlserver>/XMLPersist/default.htm` and observe the results.</span></span> <span data-ttu-id="a19d7-133">Os dados são exibidos em uma tabela DHTML vinculada.</span><span class="sxs-lookup"><span data-stu-id="a19d7-133">The data is displayed in a bound DHTML table.</span></span> 

4. <span data-ttu-id="a19d7-134">Agora, abra a `https://<sqlserver>/XMLPersist/XMLResponse.asp` URL e observe os resultados.</span><span class="sxs-lookup"><span data-stu-id="a19d7-134">Now open the URL `https://<sqlserver>/XMLPersist/XMLResponse.asp` and observe the results.</span></span> <span data-ttu-id="a19d7-135">O XML é exibido.</span><span class="sxs-lookup"><span data-stu-id="a19d7-135">The XML is displayed.</span></span>




