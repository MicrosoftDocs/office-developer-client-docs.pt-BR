---
title: Trabalhar com MSXML e System.Xml usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelos de formulário compatíveis com infopath 2003, usando msxml5, MSXML5 [InfoPath 2007],script MSXML5 [InfoPath 2007],InfoPath 2007, usando MSXML5
localization_priority: Normal
ms.assetid: f7a0cac5-26f9-49ed-b52c-0240ef0c9d38
description: Projetos de modelo de formulário que funcionam com o modelo de objeto do InfoPath 2003 usam o Microsoft XML Core Services (MSXML) internamente para trabalhar com XML. Em código gerenciado, geralmente é mais fácil usar o suporte a XML fornecido pelo namespace System.Xml na biblioteca de classes do .NET Framework. O MSXML e o System.Xml não podem trocar objetos de forma nativa, portanto, sempre que você precisar passar dados XML entre o InfoPath e outro código gerenciado, os dados XML precisam ser convertidos. Você pode trocar dados XML de System.Xml objetos com código de formulário do InfoPath usando as técnicas neste tópico.
ms.openlocfilehash: c56939a0cf03b5de6466de37013e154529afd1ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437396"
---
# <a name="working-with-msxml-and-systemxml-using-the-infopath-2003-object-model"></a>Trabalhar com MSXML e System.Xml usando o modelo de objeto do InfoPath 2003

Projetos de modelo de formulário que funcionam com o modelo de objeto do InfoPath 2003 usam o Microsoft XML Core Services (MSXML) internamente para trabalhar com XML. Em código gerenciado, geralmente é mais fácil usar o suporte a XML fornecido pelo namespace **System.Xml** na biblioteca de classes do .NET Framework. O MSXML e **oSystem.Xml** não podem trocar objetos de forma nativa, portanto, sempre que você precisar passar dados XML entre o InfoPath e outro código gerenciado, os dados XML precisam ser convertidos. Você pode trocar dados XML de **System.Xml** objetos com código de formulário do InfoPath usando as técnicas neste tópico. 
  
Para usar membros do namespaceSystem.Xmlem um projeto de código gerenciado que usa o modelo de objeto do InfoPath 2003, você deve adicionar uma referência ao **System.Xml** na guia **.NET** **da** caixa de diálogo Adicionar Referência no Visual Studio 2012.  
  
 **Anotações**
  
- Para exibir informações de referência sobre MSXML, consulte o SDK do MSXML.
    
- Membros do modelo de objeto MSXML que são empacotados pelo namespace [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) não podem ser atribuídos a representantes no código de formulário de modelos de formulário de código gerenciado. 
    
- Se você atualizar o código do seu modelo de formulário para usar o modelo  de objeto fornecido por membros do namespace [Microsoft.Office.InfoPath,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx)System.Xmlserá usado na nações. No entanto, ao fazer isso, você deve converter manualmente todo o código para usar o novo modelo de objeto. Para converter seu modelo de formulário para usar o  novo modelo de objeto, na categoria **Programação** da caixa de diálogo Opções de Formulário, clique em **Atualizar OM**.
    
## <a name="loading-an-entire-xml-document-object-model-dom-from-systemxml"></a>Carregando um dom (modelo de objeto de documento XML) inteiro System.Xml

O exemplo de código a seguir demonstra como carregar um DOM XML inteiro **System.Xml** código usando o método [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) do InfoPath e os membros do Microsoft XML Core Services que são empacotados por membros do namespace [Microsoft.Office.Interop.InfoPath.SemiTrust.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 
  
Os exemplos a seguir **exigem uma diretiva using** ou **Imports** **System.Xml** na seção de declarações do módulo de código do formulário. Além disso, como o método **Load** da  classe **XmlDocument** requer **System.Security.Permissions.FileIOPermission**,  você deve  configurar o nível de segurança do modelo de formulário como Confiança Total usando a categoria Segurança e Confiança da caixa de diálogo Opções de Formulário. 
  
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

## <a name="loading-a-single-node-from-systemxml"></a>Carregando um único nó do System.Xml

O exemplo de código a seguir mostra uma função que demonstra como clonar um único nó de um **System.Xml**. **XmlElement** usando o método MSXML **createNode** empacotado. 
  
Os exemplos a seguir **exigem uma diretiva using** ou **Imports** **System.Xml** na seção de declarações do módulo de código do formulário. 
  
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


