---
title: Rich Text e serviços da Web
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 53fddc3f-e9d9-db76-6b84-11befdb23fb0
description: 'Microsoft InfoPath suporta vinculando um controle de caixa de Rich Text em um formulário a um elemento XML que é recebido de um serviço da Web e o envio de dados de um controle de caixa de rich text para um elemento XML por meio de um serviço Web. O elemento deve seguir o formato de linguagem de marcação de hipertexto extensível (XHTML). Por exemplo, o esquema de um elemento chamado MyRichTextElement que contém texto rich teria a seguinte definição de esquema XML:'
ms.openlocfilehash: 07a7a3dbc0f054160adce54e316b01797feacd8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765702"
---
# <a name="rich-text-and-web-services"></a><span data-ttu-id="729a0-105">Rich Text e serviços da Web</span><span class="sxs-lookup"><span data-stu-id="729a0-105">Rich Text and Web Services</span></span>

<span data-ttu-id="729a0-106">Microsoft InfoPath suporta vinculando um controle de **Caixa de Rich Text** em um formulário a um elemento XML que é recebido de um serviço da Web e o envio de dados de um controle de caixa de rich text para um elemento XML por meio de um serviço Web.</span><span class="sxs-lookup"><span data-stu-id="729a0-106">Microsoft InfoPath supports binding a **Rich Text Box** control in a form to an XML element that is received from a Web service, and submitting data from a rich text box control to an XML element through a Web service.</span></span> <span data-ttu-id="729a0-107">O elemento deve seguir o formato de linguagem de marcação de hipertexto extensível (XHTML).</span><span class="sxs-lookup"><span data-stu-id="729a0-107">The element must adhere to the Extensible HyperText Markup Language (XHTML) format.</span></span> <span data-ttu-id="729a0-108">Por exemplo, o esquema de um elemento chamado `MyRichTextElement` que contém o rich text teria a seguinte definição de esquema XML:</span><span class="sxs-lookup"><span data-stu-id="729a0-108">For example, the schema for an element named  `MyRichTextElement` that contains rich text would have the following XML schema definition:</span></span> 
  
```XML
<xsd:element name="MyRichTextElement"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="http://www.w3.org/1999/xhtml" processContents="lax" 
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element>
```

<span data-ttu-id="729a0-109">Antes de um controle de **Caixa de Rich Text** pode ser vinculado com o elemento XHTML, o elemento deve ser quebrado com um nó de wrapper; Este nó wrapper pode pertencer a qualquer espaço para nome arbitrário.</span><span class="sxs-lookup"><span data-stu-id="729a0-109">Before a **Rich Text Box** control can be bound with the XHTML element, the element should be wrapped with a wrapper node; this wrapper node can belong to any arbitrary namespace.</span></span> <span data-ttu-id="729a0-110">O nó de wrapper pode ter esta aparência:</span><span class="sxs-lookup"><span data-stu-id="729a0-110">The wrapper node can look like this:</span></span> 
  
```xml
<xhtmlNode xmlns="http:// someNamespace"> 
    <div xmlns="http://www.w3.org/1999/xhtml">Your rich text here</div> 
</xhtmlNode>
```

<span data-ttu-id="729a0-111">Este tópico descreve o processo de criação de um serviço Web que pode enviar e receber XHTML e como usar o InfoPath para ligar para os parâmetros de serviço Web.</span><span class="sxs-lookup"><span data-stu-id="729a0-111">This topic outlines the process of creating a Web service that can send and receive XHTML, and how to use InfoPath to bind to the Web service parameters.</span></span> <span data-ttu-id="729a0-112">Este tópico não fornece instruções detalhadas sobre como criar um serviço Web.</span><span class="sxs-lookup"><span data-stu-id="729a0-112">This topic does not provide detailed instructions on how to create such a Web service.</span></span> <span data-ttu-id="729a0-113">Presume-se que você já tem alguma familiaridade com trabalhando com serviços Web.</span><span class="sxs-lookup"><span data-stu-id="729a0-113">It is assumed that you already have some familiarity with working with Web services.</span></span>
  
## <a name="how-to-design-a-web-service-to-receive-and-send-xhtml"></a><span data-ttu-id="729a0-114">Como criar um serviço Web para receber e enviar XHTML</span><span class="sxs-lookup"><span data-stu-id="729a0-114">How to Design a Web Service to Receive and Send XHTML</span></span>

<span data-ttu-id="729a0-115">O serviço Web de exemplo armazena os dados XHTML que ele envia e recebe em um arquivo XML no servidor.</span><span class="sxs-lookup"><span data-stu-id="729a0-115">The example Web service stores the XHTML data that it sends and receives in an XML file on the server.</span></span> <span data-ttu-id="729a0-116">Este arquivo nomeado out.xml, atua como uma fonte de dados que armazena os dados XHTML.</span><span class="sxs-lookup"><span data-stu-id="729a0-116">This file that is named out.xml, acts as a data source that stores the XHTML data.</span></span> <span data-ttu-id="729a0-117">Há dois métodos de Web que serão expostos para permitir que um aplicativo cliente para a interface com a fonte de dados XHTML: `getXhtml` e `setXhtml`.</span><span class="sxs-lookup"><span data-stu-id="729a0-117">There are two Web methods that will be exposed to allow a client application to interface with the XHTML data source:  `getXhtml` and  `setXhtml`.</span></span> <span data-ttu-id="729a0-118">O `getXhtml` método de serviço da Web retorna um **XmlNode** que contém o XHTML que pode ser vinculado a um controle de caixa de rich text do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="729a0-118">The  `getXhtml` Web Service method returns an **XmlNode** that contains the XHTML that can be bound to an InfoPath rich text box control.</span></span> <span data-ttu-id="729a0-119">O `setXhtml` método de serviço Web aceita um **XmlNode** como os dados para armazenar no arquivo out.xml.</span><span class="sxs-lookup"><span data-stu-id="729a0-119">The  `setXhtml` Web Service method accepts an **XmlNode** as the data to store in the out.xml file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="729a0-120">Estes métodos de Web requerem instruções **using** que fazem referência os namespaces **System.IO** e **System. XML** .</span><span class="sxs-lookup"><span data-stu-id="729a0-120">These Web methods require **using** statements that reference the **System.IO** and **System.Xml** namespaces.</span></span> 
  
<span data-ttu-id="729a0-121">O `getXhtml` método de serviço Web tenta carregar os dados XML a ser retornado do arquivo na pasta Data out.xml na unidade C. Se ele falhar, porque o arquivo não for encontrado ou não contém XML válido, o método retornará um elemento **DIV** HTML vazio que faz referência ao namespace XHTML.</span><span class="sxs-lookup"><span data-stu-id="729a0-121">The  `getXhtml` Web Service method attempts to load the XML data to be returned from the out.xml file in the Data folder on drive C. If it fails, because the file is not found, or does not contain valid XML, the method will return an empty **DIV** HTML element that references the XHTML namespace.</span></span> 
  
```cs
[WebMethod]
public XmlNode getXhtml()  
{  
            // This is the returned XmlDocument upon Query from InfoPath 
            XmlDocument document = new XmlDocument(); 
 
            // Create a wrapping node with the name of the rich text field. 
            // The "http://someNameSpace" can be any arbitrary namespace 
            XmlNode richNode = document.CreateNode 
                        (XmlNodeType.Element, "MyRichTextElement", "http://someNameSpace"); 
 
            // Temporary XmlDocument 
            XmlDocument tempDocument = new XmlDocument(); 
            try 
            { 
                // Read the saved rich text data from the local machine 
                tempDocument.Load(@"c:\Data\out.xml"); 
            } 
            catch (XmlException) 
            { 
                // If the file does not exist or content is not valid XML 
                tempDocument.LoadXml("<div xmlns=\"http://www.w3.org/1999/xhtml\"></div>"); 
            } 
 
            // Add the file content to the xml 
            richNode.AppendChild 
                        (document.ImportNode(tempDocument.DocumentElement, true)); 
 
            return richNode; 
}  

```

<span data-ttu-id="729a0-122">O `setXhtml` método de serviço Web aceita XHTML de um controle de **Caixa de Rich Text** em um formulário do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="729a0-122">The  `setXhtml` Web Service method accepts XHTML from a **Rich Text Box** control on an InfoPath form.</span></span> <span data-ttu-id="729a0-123">Porque os serviços da Web não suportam uma lista de nós, quando um campo de rich text que contém várias linhas é enviado a um serviço Web, o serviço Web apenas aceita a primeira linha e ignora o resto.</span><span class="sxs-lookup"><span data-stu-id="729a0-123">Because Web services do not support a node list, when a rich text field that contains multiple lines is sent to a Web service, the Web service only accepts the first line and ignores the rest.</span></span> 
  
<span data-ttu-id="729a0-124">O exemplo `setXhtml` método pressupõe que ele receberá um nó XML de nível superior, que, na maioria dos casos, será quebrado em um elemento **DIV** .</span><span class="sxs-lookup"><span data-stu-id="729a0-124">The sample  `setXhtml` method assumes that it will receive a top-level XML node, which in most cases will be wrapped in a **DIV** element.</span></span> <span data-ttu-id="729a0-125">Se o XML recebido não contiver um elemento de disposição, por exemplo, quando o texto dentro da **Caixa de Rich Text** controlar tem sem formatação, esse método irá detectar isso verificando se a propriedade **NodeType** indica que o XML passado é um nó de texto.</span><span class="sxs-lookup"><span data-stu-id="729a0-125">If the XML received does not contain a wrapping element, for example when text within the **Rich Text Box** control has no formatting, this method will detect this by checking whether the **NodeType** property indicates that the XML passed in is a text node.</span></span> <span data-ttu-id="729a0-126">Se o XML for um nó de texto, o método cria um elemento **DIV** e copia o conteúdo de nó de texto para a **DIV** , para que as **marcas DIV** contém um filho do nó de texto com o texto que foi enviado para o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="729a0-126">If the XML is a text node, the method creates a **DIV** element and copies the text node contents to the **DIV** so that the **DIV** contains a text node child with the text that was sent to the Web service.</span></span> <span data-ttu-id="729a0-127">O XML recebido por esse método é gravado no arquivo out.xml na pasta Data na unidade C.</span><span class="sxs-lookup"><span data-stu-id="729a0-127">The XML received by this method is written to the out.xml file in the Data folder on the drive C.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="729a0-128">O exemplo `setXhtml` método foi escrito para aceitar dados XHTML de qualquer tamanho.</span><span class="sxs-lookup"><span data-stu-id="729a0-128">The sample  `setXhtml` method was written to accept XHTML data of any size.</span></span> <span data-ttu-id="729a0-129">Na prática, você sempre deve verificar para ver a quantidade de dados está sendo enviado e definir um limite superior para a quantidade de dados que possa ser enviado.</span><span class="sxs-lookup"><span data-stu-id="729a0-129">In actual practice, you should always check to see how much data is being submitted and set an upper limit for how much data that can be submitted.</span></span> 
  
```cs
[WebMethod]  
public void setXhtml(XmlNode xn)  
{  
            XmlDocument document = new XmlDocument(); 
 
            if (xn == null) 
            { 
                // If nothing was submitted or the rich text field is empty, 
                // create a DIV that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "http://www.w3.org/1999/xhtml"); 
                // Copy the node to our own XmlDocument 
                document.AppendChild(div); 
            } 
            if (xn.NodeType == XmlNodeType.Text) 
            { 
                // If plain text is passed in, wrap it in a DIV 
                // that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "http://www.w3.org/1999/xhtml"); 
                // Copy the text to the DIV. 
                div.AppendChild(document.ImportNode(xn, true)); 
                // Copy the node to our own XmlDocument 
                document.AppendChild(div); 
            } 
            else 
            { 
                // Copy the node to our own XmlDocument 
                document.AppendChild(document.ImportNode(xn, true)); 
            } 
 
            // Save the file to the local machine 
            document.Save(@"c:\Data\out.xml"); 
}  

```

## <a name="how-to-create-an-infopath-form-that-exchanges-data-with-the-sample-web-service"></a><span data-ttu-id="729a0-130">Como criar um formulário do InfoPath que troca de dados com o serviço Web de amostra</span><span class="sxs-lookup"><span data-stu-id="729a0-130">How to Create an InfoPath Form That Exchanges Data with the Sample Web Service</span></span>

<span data-ttu-id="729a0-131">Execute as seguintes etapas para criar um formulário para testar o serviço Web de amostra.</span><span class="sxs-lookup"><span data-stu-id="729a0-131">Perform the following steps to create a form to test the sample Web service.</span></span>
  
### <a name="to-create-a-form-that-connects-to-the-sample-web-service"></a><span data-ttu-id="729a0-132">Para criar um formulário que se conecta ao serviço Web de amostra</span><span class="sxs-lookup"><span data-stu-id="729a0-132">To create a form that connects to the sample Web service</span></span>

1. <span data-ttu-id="729a0-133">Abra o designer de formulários do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="729a0-133">Open the InfoPath form designer.</span></span>
    
2. <span data-ttu-id="729a0-134">Na guia **New** , clique duas vezes em **Serviço Web** em **Modelos de formulário avançadas**.</span><span class="sxs-lookup"><span data-stu-id="729a0-134">On the **New** tab, double-click **Web Service** under **Advanced Form Templates**.</span></span>
    
3. <span data-ttu-id="729a0-135">Na caixa de diálogo **Assistente para Conexão de dados** , selecione a **data de recebimento**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="729a0-135">In the **Data Connection Wizard** dialog box, select **Receive data**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="729a0-136">Digite o endereço do serviço da Web que contém os métodos de serviço da Web de amostra e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="729a0-136">Type the address of the Web service that contains the sample Web service methods, and then click **Next**.</span></span> 
    
5. <span data-ttu-id="729a0-137">Para o método de recebimento, selecione **getXhtml** como a operação e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="729a0-137">For the receive method, select **getXhtml** as the operation, and then click **Next**.</span></span>
    
6. <span data-ttu-id="729a0-138">**GetXHTML** método Web service não usa nenhum parâmetro, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="729a0-138">The **getXHTML** Web service method takes no parameters, so click **Next**.</span></span>
    
7. <span data-ttu-id="729a0-139">Click **Finish**.</span><span class="sxs-lookup"><span data-stu-id="729a0-139">Click **Finish**.</span></span>
    
8. <span data-ttu-id="729a0-140">Na guia **dados** , no grupo **Ações de envio** , clique em **Para outros locais**e clique em **Serviço Web** para usar o mesmo serviço Web para os dados de envio.</span><span class="sxs-lookup"><span data-stu-id="729a0-140">On the **Data** tab, in the **Submit Actions** group click **To Other Locations**, and then click **Web Service** to use the same Web service to the submit data.</span></span> 
    
9. <span data-ttu-id="729a0-141">Digite o endereço do serviço da Web que contém os métodos de serviço da Web de amostra e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="729a0-141">Type the address of the Web service that contains the sample Web service methods, and then click **Next**.</span></span>
    
10. <span data-ttu-id="729a0-142">Para o método de envio, selecione **setXhtml** como a operação e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="729a0-142">For the submit method, select **setXhtml** as the operation, and then click **Next**.</span></span>
    
11. <span data-ttu-id="729a0-143">Clique em **Modificar**, expanda a pasta **dataFields** , expanda a pasta **s0:getXhtmlResponse** , expanda a pasta **getXhtmlResult** , selecione o elemento **MyRichTextElement** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="729a0-143">Click **Modify**, expand the **dataFields** folder, expand the **s0:getXhtmlResponse** folder, expand the **getXhtmlResult** folder, select the **MyRichTextElement** element, and then click **Next**.</span></span>
    
12. <span data-ttu-id="729a0-144">Click **Finish**.</span><span class="sxs-lookup"><span data-stu-id="729a0-144">Click **Finish**.</span></span>
    
13. <span data-ttu-id="729a0-145">No painel de tarefas **campos** , expanda a pasta de **dataFields** .</span><span class="sxs-lookup"><span data-stu-id="729a0-145">In the **Fields** task pane, expand the **dataFields** folder.</span></span> 
    
14. <span data-ttu-id="729a0-146">Expanda as pastas **s0:getXhtmlResponse** e **getXhtmlResult** e, em seguida, arraste o elemento **MyRichTextElement** ao formulário.</span><span class="sxs-lookup"><span data-stu-id="729a0-146">Expand the **s0:getXhtmlResponse** and **getXhtmlResult** folders, and then drag the **MyRichTextElement** element onto the form.</span></span> <span data-ttu-id="729a0-147">InfoPath reconhecerá que o elemento **MyRichTextElement** é um elemento XHTML e se usará um controle de caixa de rich text vincular a ela.</span><span class="sxs-lookup"><span data-stu-id="729a0-147">InfoPath will recognize that the **MyRichTextElement** element is an XHTML element and will use a rich text box control to bind to it.</span></span> 
    
15. <span data-ttu-id="729a0-148">Salvar ou publicar o formulário.</span><span class="sxs-lookup"><span data-stu-id="729a0-148">Save or publish the form.</span></span>
    
<span data-ttu-id="729a0-149">Para testar o formulário, abra o formulário, insira algum conteúdo de rich text como imagens, tabelas e texto formatado.</span><span class="sxs-lookup"><span data-stu-id="729a0-149">To test the form, open the form, enter some rich text content such as pictures, tables, and formatted text.</span></span> <span data-ttu-id="729a0-150">Clique em **Enviar** na faixa de opções para armazenar o conteúdo de rich text no arquivo out.xml no servidor.</span><span class="sxs-lookup"><span data-stu-id="729a0-150">Click **Submit** on the ribbon to store the rich text content in the out.xml file on the server.</span></span> <span data-ttu-id="729a0-151">Clique em **consulta** , na guia **Exibir** e, em seguida, clique no botão **Executar consulta** no formulário.</span><span class="sxs-lookup"><span data-stu-id="729a0-151">Click **Query** on the **View** tab, and then click the **Run Query** button on the form.</span></span> <span data-ttu-id="729a0-152">O controle de **Caixa de Rich Text** deve exibir o conteúdo XHTML do arquivo out.xml exe.</span><span class="sxs-lookup"><span data-stu-id="729a0-152">The **Rich Text Box** control should display the XHTML content from the out.xml file.</span></span> <span data-ttu-id="729a0-153">Se o campo de rich text contiver várias linhas, o serviço da Web apenas aceitar a primeira linha e ignorar o restante.</span><span class="sxs-lookup"><span data-stu-id="729a0-153">If the rich text field contains multiple lines, the Web service will only accept the first line and ignore the rest.</span></span> 
  

