---
title: Trabalhando com MSXML e System. XML usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelos de formulário de 2003 compatíveis do InfoPath, usando msxml5, MSXML5 [InfoPath 2007], MSXML5 script [InfoPath 2007], InfoPath 2007, usando MSXML5
localization_priority: Normal
ms.assetid: f7a0cac5-26f9-49ed-b52c-0240ef0c9d38
description: Projetos de modelo de formulário que funcionam com o modelo de objeto do InfoPath 2003 usam o Microsoft XML Core Services (MSXML) internamente para trabalhar com o XML. Em código gerenciado, geralmente é mais fácil de usar o suporte a XML fornecido pelo namespace System. XML na biblioteca de classes .NET Framework. MSXML e System. XML não podem trocar objetos nativamente, portanto, sempre que você precisa passar dados XML entre o InfoPath e outro código gerenciado, os dados XML precisam ser convertido. Você pode trocar dados XML dos objetos System. XML com o código de formulário do InfoPath usando as técnicas neste tópico.
ms.openlocfilehash: 345aeb3dcb6e9621657bd2b21f98c87cb5e61993
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765712"
---
# <a name="working-with-msxml-and-systemxml-using-the-infopath-2003-object-model"></a>Trabalhando com MSXML e System. XML usando o modelo de objeto do InfoPath 2003

Projetos de modelo de formulário que funcionam com o modelo de objeto do InfoPath 2003 usam o Microsoft XML Core Services (MSXML) internamente para trabalhar com o XML. Em código gerenciado, geralmente é mais fácil de usar o suporte a XML fornecido pelo namespace **System. XML** na biblioteca de classes .NET Framework. MSXML e **System. XML** não podem trocar objetos nativamente, portanto, sempre que você precisa passar dados XML entre o InfoPath e outro código gerenciado, os dados XML precisam ser convertido. Você pode trocar dados XML dos objetos **System. XML** com o código de formulário do InfoPath usando as técnicas neste tópico. 
  
Para usar os membros do namespace **System. XML** em um projeto de código gerenciado que utiliza o modelo de objeto do InfoPath 2003, você deve adicionar uma referência ao **System. XML** na guia **.NET** , da caixa de diálogo **Adicionar referência** no Visual Studio 2012. 
  
 **Notes**
  
- Para exibir informações de referência sobre MSXML, consulte o SDK do MSXML.
    
- Membros do modelo de objeto MSXML que devem ser quebrados pelo namespace [SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) não podem ser atribuídos aos delegados no código do formulário de modelos de formulário de código gerenciado. 
    
- Se você atualizar o código do seu modelo de formulário para usar o modelo de objeto fornecido pelos membros do namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , **System. XML** é usado nativamente. No entanto, ao fazer isso, você deve converter todos do seu código para usar o novo modelo de objeto manualmente. Para converter o seu modelo de formulário para usar o novo modelo de objeto, na categoria **programação** da caixa de diálogo **Opções de formulário** , clique em **Atualizar OM**.
    
## <a name="loading-an-entire-xml-document-object-model-dom-from-systemxml"></a>Carregar um modelo de objeto de documento XML inteira (DOM) do System. XML

O exemplo de código a seguir demonstra como carregar um inteiro DOM do XML do código de **System. XML** usando o método InfoPath [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) e os membros do Microsoft XML Core Services que devem ser quebradas por membros do [ SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace. 
  
Os exemplos a seguir exigem um **uso** ou a diretiva de **importações** para **System. XML** na seção Declaração do módulo do formulário de código. Além disso, como o método **Load** da classe **XmlDocument** requer **System.Security.Permissions.FileIOPermission**, você deve configurar o nível de segurança do modelo de formulário como **Confiança total** usando a segurança de ** e confie** categoria da caixa de diálogo **Opções de formulário** . 
  
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

## <a name="loading-a-single-node-from-systemxml"></a>Carregando um único nó de System. XML

O exemplo de código a seguir mostra uma função que demonstra como clonar a um único nó de um **System. XML**. Usando o método de **createNode** MSXML ajustado **XmlElement** . 
  
Os exemplos a seguir exigem um **uso** ou a diretiva de **importações** para **System. XML** na seção Declaração do módulo do formulário de código. 
  
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


