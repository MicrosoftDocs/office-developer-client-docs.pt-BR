---
title: Trabalhar com MSXML e System.Xml usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelos de formulário compatíveis com o InfoPath 2003, usando o Msxml5, MSXML5 [InfoPath 2007], MSXML5 script [InfoPath 2007], InfoPath 2007, usando MSXML5
localization_priority: Normal
ms.assetid: f7a0cac5-26f9-49ed-b52c-0240ef0c9d38
description: Projetos de modelo de formulário que funcionam com o modelo de objeto do InfoPath 2003 usam o Microsoft XML Core Services (MSXML) internamente para trabalhar com XML. Em código gerenciado, geralmente é mais fácil usar o suporte a XML fornecido pelo namespace System. xml na biblioteca de classes do .NET Framework. MSXML e System. xml não podem trocar objetos nativamente, portanto, sempre que você precisar transmitir dados XML entre o InfoPath e outros códigos gerenciados, os dados XML precisarão ser convertidos. Você pode trocar dados XML de objetos System. XML com o código de formulário do InfoPath usando as técnicas neste tópico.
ms.openlocfilehash: c56939a0cf03b5de6466de37013e154529afd1ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437396"
---
# <a name="working-with-msxml-and-systemxml-using-the-infopath-2003-object-model"></a><span data-ttu-id="c0e67-107">Trabalhar com MSXML e System.Xml usando o modelo de objeto do InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="c0e67-107">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="c0e67-108">Projetos de modelo de formulário que funcionam com o modelo de objeto do InfoPath 2003 usam o Microsoft XML Core Services (MSXML) internamente para trabalhar com XML.</span><span class="sxs-lookup"><span data-stu-id="c0e67-108">Form template projects that work with the InfoPath 2003 object model use Microsoft XML Core Services (MSXML) internally to work with XML.</span></span> <span data-ttu-id="c0e67-109">Em código gerenciado, geralmente é mais fácil usar o suporte a XML fornecido pelo namespace **System. xml** na biblioteca de classes do .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c0e67-109">In managed code, it is often easier to use the XML support provided by the **System.Xml** namespace in the .NET Framework class library.</span></span> <span data-ttu-id="c0e67-110">MSXML e **System. xml** não podem trocar objetos nativamente, portanto, sempre que você precisar transmitir dados XML entre o InfoPath e outros códigos gerenciados, os dados XML precisarão ser convertidos.</span><span class="sxs-lookup"><span data-stu-id="c0e67-110">MSXML and **System.Xml** cannot exchange objects natively, so whenever you need to pass XML data between InfoPath and other managed code, XML data needs to be converted.</span></span> <span data-ttu-id="c0e67-111">Você pode trocar dados XML de objetos **System. xml** com o código de formulário do InfoPath usando as técnicas neste tópico.</span><span class="sxs-lookup"><span data-stu-id="c0e67-111">You can exchange XML data from **System.Xml** objects with InfoPath form code by using the techniques in this topic.</span></span> 
  
<span data-ttu-id="c0e67-112">Para usar membros do namespace **System. xml** em um projeto de código gerenciado que usa o modelo de objeto do InfoPath 2003, você deve adicionar uma referência a **System. xml** na guia **.net** da caixa de diálogo **Adicionar referência** no Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="c0e67-112">To use members of the **System.Xml** namespace in a managed code project that uses the InfoPath 2003 object model, you must add a reference to **System.Xml** on the **.NET** tab of the **Add Reference** dialog box in Visual Studio 2012.</span></span> 
  
 <span data-ttu-id="c0e67-113">**Anotações**</span><span class="sxs-lookup"><span data-stu-id="c0e67-113">**Notes**</span></span>
  
- <span data-ttu-id="c0e67-114">Para exibir informações de referência sobre o MSXML, consulte o SDK do MSXML.</span><span class="sxs-lookup"><span data-stu-id="c0e67-114">To view reference information about MSXML, see the MSXML SDK.</span></span>
    
- <span data-ttu-id="c0e67-115">Os membros do modelo de objeto do MSXML que são empacotados pelo namespace [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) não podem ser atribuídos a representantes no código de formulário de modelos de formulário de código gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c0e67-115">Members of the MSXML object model that are wrapped by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace cannot be assigned to delegates in the form code of managed-code form templates.</span></span> 
    
- <span data-ttu-id="c0e67-116">Se você atualizar o código do seu modelo de formulário para usar o modelo de objeto fornecido pelos membros do namespace [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , **System. xml** será usado nativamente.</span><span class="sxs-lookup"><span data-stu-id="c0e67-116">If you update the code of your form template to use the object model provided by members of the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace, **System.Xml** is used natively.</span></span> <span data-ttu-id="c0e67-117">No enTanto, ao fazer isso, você deve converter manualmente todo o seu código para usar o novo modelo de objeto.</span><span class="sxs-lookup"><span data-stu-id="c0e67-117">However, when doing so, you must manually convert all of your code to use the new object model.</span></span> <span data-ttu-id="c0e67-118">Para converter o modelo de formulário para usar o novo modelo de objeto, na categoria **programação** da caixa de diálogo **Opções de formulário** , clique em **Atualizar OM**.</span><span class="sxs-lookup"><span data-stu-id="c0e67-118">To convert your form template to use the new object model, in the **Programming** category of the **Form Options** dialog box, click **Upgrade OM**.</span></span>
    
## <a name="loading-an-entire-xml-document-object-model-dom-from-systemxml"></a><span data-ttu-id="c0e67-119">Carregando um modelo de objeto de documento XML (DOM) inteiro de System. xml</span><span class="sxs-lookup"><span data-stu-id="c0e67-119">Loading an Entire XML Document Object Model (DOM) from System.Xml</span></span>

<span data-ttu-id="c0e67-120">O exemplo de código a seguir demonstra como carregar um DOM XML inteiro do código **System. xml** usando o método [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) do InfoPath e os membros do Microsoft XML Core Services que são empacotados por membros do [ Namespace Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c0e67-120">The following code sample demonstrates how to load an entire XML DOM from **System.Xml** code using the InfoPath [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) method and the members of Microsoft XML Core Services that are wrapped by members of the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
<span data-ttu-id="c0e67-121">Os exemplos a seguir exigem uma diretiva **using** ou Imports para **System. xml** na seção declaração do módulo de código de formulário. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c0e67-121">The following examples require a **using** or **Imports** directive for **System.Xml** in the declarations section of the form code module.</span></span> <span data-ttu-id="c0e67-122">Além disso, como o método **Load** da classe **XmlDocument** requer **System. Security. Permissions. FileIOPermission**, você deve configurar o nível de segurança do modelo de formulário como **confiança total** usando a **segurança e** a categoria de confiança da caixa de diálogo **Opções de formulário** .</span><span class="sxs-lookup"><span data-stu-id="c0e67-122">Additionally, because the **Load** method of the **XmlDocument** class requires **System.Security.Permissions.FileIOPermission**, you must configure the security level of the form template as **Full Trust** using the **Security and Trust** category of the **Form Options** dialog box.</span></span> 
  
```cs
// Create a System.Xml XmlDocument and load an XML file.
XmlDocument doc = new XmlDocument();
doc.Load("c:\\temp\\MyFile.xml");
// Create an MSXML DOM object.
IXMLDOMDocument newDoc = thisXDocument.CreateDOM();
// Load the DOM with the XML from the System.XML object.
newDoc.loadXML(doc.DocumentElement.OuterXml);
```

```vb
' Create a System.Xml XmlDocument and load an XML file.
Dim doc As XmlDocument = New XmlDocument()
doc.Load("c:\temp\MyFile.xml");
' Create an MSXML DOM object.
Dim newDoc As IXMLDOMDocument = thisXDocument.CreateDOM()
' Load the DOM with the XML from the System.XML object.
newDoc.loadXML(doc.DocumentElement.OuterXml)
```

## <a name="loading-a-single-node-from-systemxml"></a><span data-ttu-id="c0e67-123">Carregar um único nó de System. xml</span><span class="sxs-lookup"><span data-stu-id="c0e67-123">Loading a Single Node from System.Xml</span></span>

<span data-ttu-id="c0e67-124">O exemplo de código a seguir mostra uma função que demonstra como clonar um único nó de um **System. xml**.</span><span class="sxs-lookup"><span data-stu-id="c0e67-124">The following code sample shows a function that demonstrates how to clone a single node from a **System.Xml**.</span></span> <span data-ttu-id="c0e67-125">**XmlElement** usando o método **SetNode** do MSXML encapsulado.</span><span class="sxs-lookup"><span data-stu-id="c0e67-125">**XmlElement** using the wrapped MSXML **createNode** method.</span></span> 
  
<span data-ttu-id="c0e67-126">Os exemplos a seguir exigem uma diretiva **using** ou Imports para **System. xml** na seção declaração do módulo de código de formulário. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c0e67-126">The following examples require a **using** or **Imports** directive for **System.Xml** in the declarations section of the form code module.</span></span> 
  
```cs
// This function takes a System.Xml XmlElement object and 
// an MSXML IXMLDOMDocument object, and returns an MSXML 
// IXMLDOMNode object that is a copy of the XmlElement object.
public IXMLDOMNode CloneSystemXmlElementToMsxml(
   XmlElement systemXmlElement, IXMLDOMDocument msxmlDocument)
{
   IXMLDOMNode msxmlResultNode;
   // Create a new element from the MSXML DOM using the same 
   // namespace as the XmlElement.
   msxmlResultNode = msxmlDocument.createNode(
      DOMNodeType.NODE_ELEMENT, 
      systemXmlElement.Name, 
      systemXmlElement.NamespaceURI);
   // Set the element's value.
   msxmlResultNode.text = systemXmlElement.Value.ToString();
   return msxmlResultNode;
}
```

```vb
' This function takes a System.Xml XmlElement object and 
' an MSXML IXMLDOMDocument object, and returns an MSXML 
' IXMLDOMNode object that is a copy of the XmlElement object.
Public Function CloneSystemXmlElementToMsxml(_
   XmlElement systemXmlElement, _
   IXMLDOMDocument msxmlDocument) As IXMLDOMNode
   Dim msxmlResultNode As IXMLDOMNode
   ' Create a new element from the MSXML DOM using the same 
   ' namespace as the XmlElement.
   msxmlResultNode = msxmlDocument.createNode(_
      DOMNodeType.NODE_ELEMENT, _
      systemXmlElement.Name, _
      systemXmlElement.NamespaceURI)
   ' Set the element's value.
   msxmlResultNode.text = systemXmlElement.Value.ToString()
   Return msxmlResultNode
End Function
```


