---
title: Rich Text e Serviços Web
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 53fddc3f-e9d9-db76-6b84-11befdb23fb0
description: 'O Microsoft InfoPath dá suporte à associação de um controle de Caixa RTF em um formulário a um elemento XML que é recebido de um serviço Web, e ao envio de dados de um controle de caixa RTF para um elemento XML por meio de um serviço Web. O elemento deve seguir o formato Extensible HTML (XHTML). Por exemplo, o esquema de um elemento chamado MyRichTextElement que contenha RTF teria a seguinte definição de esquema XML:'
ms.openlocfilehash: d10f4a8cedcff43d1c351068859aee0edf607c81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299843"
---
# <a name="rich-text-and-web-services"></a><span data-ttu-id="5150a-105">Rich Text e Serviços Web</span><span class="sxs-lookup"><span data-stu-id="5150a-105">Rich Text and Web Services</span></span>

<span data-ttu-id="5150a-106">O Microsoft InfoPath dá suporte à associação de um controle de **Caixa RTF** em um formulário a um elemento XML que é recebido de um serviço Web, e ao envio de dados de um controle de caixa RTF para um elemento XML por meio de um serviço Web.</span><span class="sxs-lookup"><span data-stu-id="5150a-106">Microsoft InfoPath supports binding a **Rich Text Box** control in a form to an XML element that is received from a Web service, and submitting data from a rich text box control to an XML element through a Web service.</span></span> <span data-ttu-id="5150a-107">O elemento deve seguir o formato Extensible HTML (XHTML).</span><span class="sxs-lookup"><span data-stu-id="5150a-107">The element must adhere to the Extensible HyperText Markup Language (XHTML) format.</span></span> <span data-ttu-id="5150a-108">Por exemplo, o esquema de um elemento chamado `MyRichTextElement` que contém RTF deve ter a seguinte definição de esquema XML:</span><span class="sxs-lookup"><span data-stu-id="5150a-108">For example, the schema for an element named  `MyRichTextElement` that contains rich text would have the following XML schema definition:</span></span> 
  
```XML
<xsd:element name="MyRichTextElement"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="https://www.w3.org/1999/xhtml" processContents="lax" 
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element>
```

<span data-ttu-id="5150a-109">Antes que um controle de **Caixa RTF** possa ser associado com o elemento XHTML, o elemento deve ser encapsulado com um nó de wrapper, que pode pertencer a qualquer namespace arbitrário.</span><span class="sxs-lookup"><span data-stu-id="5150a-109">Before a **Rich Text Box** control can be bound with the XHTML element, the element should be wrapped with a wrapper node; this wrapper node can belong to any arbitrary namespace.</span></span> <span data-ttu-id="5150a-110">O nó de wrapper pode ter esta aparência:</span><span class="sxs-lookup"><span data-stu-id="5150a-110">The wrapper node can look like this:</span></span> 
  
```xml
<xhtmlNode xmlns="https:// someNamespace"> 
    <div xmlns="https://www.w3.org/1999/xhtml">Your rich text here</div> 
</xhtmlNode>
```

<span data-ttu-id="5150a-111">Este tópico descreve o processo de criação de um serviço Web que pode enviar e receber XHTML, além de como usar o InfoPath para se associar aos parâmetros de serviço Web.</span><span class="sxs-lookup"><span data-stu-id="5150a-111">This topic outlines the process of creating a Web service that can send and receive XHTML, and how to use InfoPath to bind to the Web service parameters.</span></span> <span data-ttu-id="5150a-112">Este tópico fornece instruções detalhadas sobre como criar tal serviço Web.</span><span class="sxs-lookup"><span data-stu-id="5150a-112">This topic does not provide detailed instructions on how to create such a Web service.</span></span> <span data-ttu-id="5150a-113">Supomos que você já saiba um pouco sobre como trabalhar com serviços Web.</span><span class="sxs-lookup"><span data-stu-id="5150a-113">It is assumed that you already have some familiarity with working with Web services.</span></span>
  
## <a name="how-to-design-a-web-service-to-receive-and-send-xhtml"></a><span data-ttu-id="5150a-114">Como projetar um serviço Web para receber e enviar XHTML</span><span class="sxs-lookup"><span data-stu-id="5150a-114">How to Design a Web Service to Receive and Send XHTML</span></span>

<span data-ttu-id="5150a-115">O serviço Web de exemplo armazena dados XHTML que envia e recebe em um arquivo XML no servidor.</span><span class="sxs-lookup"><span data-stu-id="5150a-115">The example Web service stores the XHTML data that it sends and receives in an XML file on the server.</span></span> <span data-ttu-id="5150a-116">Esse arquivo é denominado out.xml, e funciona como uma fonte de dados que armazena os dados XHTML.</span><span class="sxs-lookup"><span data-stu-id="5150a-116">This file that is named out.xml, acts as a data source that stores the XHTML data.</span></span> <span data-ttu-id="5150a-117">Há dois métodos Web que serão expostos para permitir que um aplicativo cliente se comunique com a fonte de dados XHTML: `getXhtml` e `setXhtml`.</span><span class="sxs-lookup"><span data-stu-id="5150a-117">There are two Web methods that will be exposed to allow a client application to interface with the XHTML data source:  `getXhtml` and  `setXhtml`.</span></span> <span data-ttu-id="5150a-118">O método de Serviço Web `getXhtml` retorna um **XmlNode** que contém o XHTML que pode ser associado a um controle de Caixa RTF do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="5150a-118">The  `getXhtml` Web Service method returns an **XmlNode** that contains the XHTML that can be bound to an InfoPath rich text box control.</span></span> <span data-ttu-id="5150a-119">O método de Serviço Web `setXhtml` aceita um **XmlNode** como os dados a serem armazenados no arquivo out.xml.</span><span class="sxs-lookup"><span data-stu-id="5150a-119">The  `setXhtml` Web Service method accepts an **XmlNode** as the data to store in the out.xml file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5150a-120">Esses métodos Web exigem instruções **using** que fazem referência aos namespaces **System.IO** e **System.XML**.</span><span class="sxs-lookup"><span data-stu-id="5150a-120">These Web methods require **using** statements that reference the **System.IO** and **System.Xml** namespaces.</span></span> 
  
<span data-ttu-id="5150a-121">O método de Serviço Web `getXhtml` tenta carregar os dados XML a serem retornados do arquivo out.xml na pasta Data da unidade C. Se ele não conseguir, porque o arquivo não foi encontrado ou por não conter XML válido, o método retornará um elemento HTML **DIV** vazio que se refere ao namespace XHTML.</span><span class="sxs-lookup"><span data-stu-id="5150a-121">The  `getXhtml` Web Service method attempts to load the XML data to be returned from the out.xml file in the Data folder on drive C. If it fails, because the file is not found, or does not contain valid XML, the method will return an empty **DIV** HTML element that references the XHTML namespace.</span></span> 
  
```cs
[WebMethod]
public XmlNode getXhtml()  
{  
            // This is the returned XmlDocument upon Query from InfoPath 
            XmlDocument document = new XmlDocument(); 
 
            // Create a wrapping node with the name of the rich text field. 
            // The "https://someNameSpace" can be any arbitrary namespace 
            XmlNode richNode = document.CreateNode 
                        (XmlNodeType.Element, "MyRichTextElement", "https://someNameSpace"); 
 
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
                tempDocument.LoadXml("<div xmlns=\"https://www.w3.org/1999/xhtml\"></div>"); 
            } 
 
            // Add the file content to the xml 
            richNode.AppendChild 
                        (document.ImportNode(tempDocument.DocumentElement, true)); 
 
            return richNode; 
}  

```

<span data-ttu-id="5150a-122">O método de Serviço Web `setXhtml` aceita XHTML de um controle **Caixa RTF** em um formulário do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="5150a-122">The  `setXhtml` Web Service method accepts XHTML from a **Rich Text Box** control on an InfoPath form.</span></span> <span data-ttu-id="5150a-123">Como os Serviços Web não têm suporte para uma lista de nós, quando um campo rich text com várias linhas é enviado para um serviço Web, o serviço Web apenas aceita a primeira linha e ignora o restante.</span><span class="sxs-lookup"><span data-stu-id="5150a-123">Because Web services do not support a node list, when a rich text field that contains multiple lines is sent to a Web service, the Web service only accepts the first line and ignores the rest.</span></span> 
  
<span data-ttu-id="5150a-124">O método `setXhtml` de exemplo supõe que receberá um nó XML de nível superior, que na maioria dos casos estará encapsulado em um elemento **DIV**.</span><span class="sxs-lookup"><span data-stu-id="5150a-124">The sample  `setXhtml` method assumes that it will receive a top-level XML node, which in most cases will be wrapped in a **DIV** element.</span></span> <span data-ttu-id="5150a-125">Se o XML recebido não contiver um elemento de encapsulamento, como quando o texto dentro do controle de **Caixa RTF** não tem formatação, esse método detectará isso, verificando se a propriedade **NodeType** indica que o XML passado está em um nó de texto.</span><span class="sxs-lookup"><span data-stu-id="5150a-125">If the XML received does not contain a wrapping element, for example when text within the **Rich Text Box** control has no formatting, this method will detect this by checking whether the **NodeType** property indicates that the XML passed in is a text node.</span></span> <span data-ttu-id="5150a-126">Se o XML for um nó de texto, o método criará um elemento **DIV** e copiará o conteúdo do nó de texto para o **DIV**, para que o **DIV** contenha um nó de texto filho com o texto que foi enviado para o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="5150a-126">If the XML is a text node, the method creates a **DIV** element and copies the text node contents to the **DIV** so that the **DIV** contains a text node child with the text that was sent to the Web service.</span></span> <span data-ttu-id="5150a-127">O XML recebido por esse método é gravado no arquivo out.xml na pasta Data da unidade C.</span><span class="sxs-lookup"><span data-stu-id="5150a-127">The XML received by this method is written to the out.xml file in the Data folder on the drive C.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5150a-128">O método `setXhtml` de exemplo foi elaborado para aceitar dados XHTML de qualquer tamanho.</span><span class="sxs-lookup"><span data-stu-id="5150a-128">The sample  `setXhtml` method was written to accept XHTML data of any size.</span></span> <span data-ttu-id="5150a-129">Na prática, você deve sempre verificar a quantidade de dados que estão sendo enviados e definir um limite máximo para a quantidade de dados que podem ser enviados.</span><span class="sxs-lookup"><span data-stu-id="5150a-129">In actual practice, you should always check to see how much data is being submitted and set an upper limit for how much data that can be submitted.</span></span> 
  
```cs
[WebMethod]  
public void setXhtml(XmlNode xn)  
{  
            XmlDocument document = new XmlDocument(); 
 
            if (xn == null) 
            { 
                // If nothing was submitted or the rich text field is empty, 
                // create a DIV that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "https://www.w3.org/1999/xhtml"); 
                // Copy the node to our own XmlDocument 
                document.AppendChild(div); 
            } 
            if (xn.NodeType == XmlNodeType.Text) 
            { 
                // If plain text is passed in, wrap it in a DIV 
                // that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "https://www.w3.org/1999/xhtml"); 
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

## <a name="how-to-create-an-infopath-form-that-exchanges-data-with-the-sample-web-service"></a><span data-ttu-id="5150a-130">Como criar um formulário do InfoPath que troca dados com o serviço Web de exemplo</span><span class="sxs-lookup"><span data-stu-id="5150a-130">How to Create an InfoPath Form That Exchanges Data with the Sample Web Service</span></span>

<span data-ttu-id="5150a-131">Execute as etapas a seguir para criar um formulário para testar o serviço Web de exemplo.</span><span class="sxs-lookup"><span data-stu-id="5150a-131">Perform the following steps to create a form to test the sample Web service.</span></span>
  
### <a name="to-create-a-form-that-connects-to-the-sample-web-service"></a><span data-ttu-id="5150a-132">Para criar um formulário que se conecta ao serviço Web de exemplo</span><span class="sxs-lookup"><span data-stu-id="5150a-132">To create a form that connects to the sample Web service</span></span>

1. <span data-ttu-id="5150a-133">Abra o designer de formulário do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="5150a-133">Open the InfoPath form designer.</span></span>
    
2. <span data-ttu-id="5150a-134">Na guia **Novo**, clique duas vezes em **Serviço Web** sob **Modelos de Formulário Avançados**.</span><span class="sxs-lookup"><span data-stu-id="5150a-134">On the **New** tab, double-click **Web Service** under **Advanced Form Templates**.</span></span>
    
3. <span data-ttu-id="5150a-135">Na caixa de diálogo **Assistente de Conexão de Dados**, selecione **Receber dados** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="5150a-135">In the **Data Connection Wizard** dialog box, select **Receive data**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="5150a-136">Digite o endereço do serviço Web que contém os métodos de serviço Web de exemplo e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="5150a-136">Type the address of the Web service that contains the sample Web service methods, and then click **Next**.</span></span> 
    
5. <span data-ttu-id="5150a-137">Para o método de recebimento, selecione **getXhtml** como a operação e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="5150a-137">For the receive method, select **getXhtml** as the operation, and then click **Next**.</span></span>
    
6. <span data-ttu-id="5150a-138">O método do serviço Web **getXHTML** não recebe parâmetros, portanto, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="5150a-138">The **getXHTML** Web service method takes no parameters, so click **Next**.</span></span>
    
7. <span data-ttu-id="5150a-139">Clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="5150a-139">Click **Finish**.</span></span>
    
8. <span data-ttu-id="5150a-140">Na guia **Dados**, no grupo **Enviar Ações**, clique em **Para Outros Locais** e clique em **Serviço Web** para usar o mesmo serviço Web para enviar dados.</span><span class="sxs-lookup"><span data-stu-id="5150a-140">On the **Data** tab, in the **Submit Actions** group click **To Other Locations**, and then click **Web Service** to use the same Web service to the submit data.</span></span> 
    
9. <span data-ttu-id="5150a-141">Digite o endereço do serviço Web que contém os métodos de serviço Web de exemplo e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="5150a-141">Type the address of the Web service that contains the sample Web service methods, and then click **Next**.</span></span>
    
10. <span data-ttu-id="5150a-142">Para o método de envio, escolha **setXhtml** como a operação e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="5150a-142">For the submit method, select **setXhtml** as the operation, and then click **Next**.</span></span>
    
11. <span data-ttu-id="5150a-143">Clique em **Modificar**, expanda a pasta **dataFields**, expanda a pasta **s0:getXhtmlResponse**, expanda a pasta **getXhtmlResult**, selecione o elemento **MyRichTextElement** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="5150a-143">Click **Modify**, expand the **dataFields** folder, expand the **s0:getXhtmlResponse** folder, expand the **getXhtmlResult** folder, select the **MyRichTextElement** element, and then click **Next**.</span></span>
    
12. <span data-ttu-id="5150a-144">Clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="5150a-144">Click **Finish**.</span></span>
    
13. <span data-ttu-id="5150a-145">No painel de tarefas **Campos**, expanda a pasta **dataFields**.</span><span class="sxs-lookup"><span data-stu-id="5150a-145">In the **Fields** task pane, expand the **dataFields** folder.</span></span> 
    
14. <span data-ttu-id="5150a-146">Expanda as pastas **s0:getXhtmlResponse** e **getXhtmlResult** e arraste o elemento **MyRichTextElement** para o formulário.</span><span class="sxs-lookup"><span data-stu-id="5150a-146">Expand the **s0:getXhtmlResponse** and **getXhtmlResult** folders, and then drag the **MyRichTextElement** element onto the form.</span></span> <span data-ttu-id="5150a-147">O InfoPath reconhecerá que o elemento **MyRichTextElement** é um elemento XHTML e usará um controle de caixa RTF para associar a ele.</span><span class="sxs-lookup"><span data-stu-id="5150a-147">InfoPath will recognize that the **MyRichTextElement** element is an XHTML element and will use a rich text box control to bind to it.</span></span> 
    
15. <span data-ttu-id="5150a-148">Salve ou publique o formulário.</span><span class="sxs-lookup"><span data-stu-id="5150a-148">Save or publish the form.</span></span>
    
<span data-ttu-id="5150a-149">Para testar o formulário, abra-o, insira algum conteúdo rich text, como imagens, tabelas e texto formatado.</span><span class="sxs-lookup"><span data-stu-id="5150a-149">To test the form, open the form, enter some rich text content such as pictures, tables, and formatted text.</span></span> <span data-ttu-id="5150a-150">Clique em **Enviar** na faixa de opções para armazenar conteúdo rich text no arquivo out.xml no servidor.</span><span class="sxs-lookup"><span data-stu-id="5150a-150">Click **Submit** on the ribbon to store the rich text content in the out.xml file on the server.</span></span> <span data-ttu-id="5150a-151">Clique em **Consulta** na guia **Exibir** e clique no botão **Executar Consulta** no formulário.</span><span class="sxs-lookup"><span data-stu-id="5150a-151">Click **Query** on the **View** tab, and then click the **Run Query** button on the form.</span></span> <span data-ttu-id="5150a-152">O controle **Caixa RTF** deverá exibir o conteúdo XHTML do arquivo out.xml.</span><span class="sxs-lookup"><span data-stu-id="5150a-152">The **Rich Text Box** control should display the XHTML content from the out.xml file.</span></span> <span data-ttu-id="5150a-153">Se o campo rich text contiver várias linhas, o serviço Web somente aceitará a primeira linha e ignorará o restante.</span><span class="sxs-lookup"><span data-stu-id="5150a-153">If the rich text field contains multiple lines, the Web service will only accept the first line and ignore the rest.</span></span> 
  

