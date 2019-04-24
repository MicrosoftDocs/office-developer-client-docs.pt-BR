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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299717"
---
# <a name="working-with-msxml-and-systemxml-using-the-infopath-2003-object-model"></a>Trabalhar com MSXML e System.Xml usando o modelo de objeto do InfoPath 2003

Projetos de modelo de formulário que funcionam com o modelo de objeto do InfoPath 2003 usam o Microsoft XML Core Services (MSXML) internamente para trabalhar com XML. Em código gerenciado, geralmente é mais fácil usar o suporte a XML fornecido pelo namespace **System. xml** na biblioteca de classes do .NET Framework. MSXML e **System. xml** não podem trocar objetos nativamente, portanto, sempre que você precisar transmitir dados XML entre o InfoPath e outros códigos gerenciados, os dados XML precisarão ser convertidos. Você pode trocar dados XML de objetos **System. xml** com o código de formulário do InfoPath usando as técnicas neste tópico. 
  
Para usar membros do namespace **System. xml** em um projeto de código gerenciado que usa o modelo de objeto do InfoPath 2003, você deve adicionar uma referência a **System. xml** na guia **.net** da caixa de diálogo **Adicionar referência** no Visual Studio 2012. 
  
 **Anotações**
  
- Para exibir informações de referência sobre o MSXML, consulte o SDK do MSXML.
    
- Os membros do modelo de objeto do MSXML que são empacotados pelo namespace [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) não podem ser atribuídos a representantes no código de formulário de modelos de formulário de código gerenciado. 
    
- Se você atualizar o código do seu modelo de formulário para usar o modelo de objeto fornecido pelos membros do namespace [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , **System. xml** será usado nativamente. No enTanto, ao fazer isso, você deve converter manualmente todo o seu código para usar o novo modelo de objeto. Para converter o modelo de formulário para usar o novo modelo de objeto, na categoria **programação** da caixa de diálogo **Opções de formulário** , clique em **Atualizar OM**.
    
## <a name="loading-an-entire-xml-document-object-model-dom-from-systemxml"></a>Carregando um modelo de objeto de documento XML (DOM) inteiro de System. xml

O exemplo de código a seguir demonstra como carregar um DOM XML inteiro do código **System. xml** usando o método [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) do InfoPath e os membros do Microsoft XML Core Services que são empacotados por membros do [ Namespace Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
  
Os exemplos a seguir exigem uma diretiva **using** ou Imports para **System. xml** na seção declaração do módulo de código de formulário. **** Além disso, como o método **Load** da classe **XmlDocument** requer **System. Security. Permissions. FileIOPermission**, você deve configurar o nível de segurança do modelo de formulário como **confiança total** usando a **segurança e** a categoria de confiança da caixa de diálogo **Opções de formulário** . 
  
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

## <a name="loading-a-single-node-from-systemxml"></a>Carregar um único nó de System. xml

O exemplo de código a seguir mostra uma função que demonstra como clonar um único nó de um **System. xml**. **XmlElement** usando o método **SetNode** do MSXML encapsulado. 
  
Os exemplos a seguir exigem uma diretiva **using** ou Imports para **System. xml** na seção declaração do módulo de código de formulário. **** 
  
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


