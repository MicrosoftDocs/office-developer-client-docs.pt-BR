---
title: Rich Text e Serviços Web
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 53fddc3f-e9d9-db76-6b84-11befdb23fb0
description: 'O Microsoft InfoPath dá suporte à associação de um controle de Caixa RTF em um formulário a um elemento XML que é recebido de um serviço Web e ao envio de dados de um controle de caixa RTF para um elemento XML por meio de um serviço Web. O elemento deve seguir o formato Extensible HTML (XHTML). Por exemplo, o esquema de um elemento chamado MyRichTextElement que contenha RTF teria a seguinte definição de esquema XML:'
ms.openlocfilehash: d10f4a8cedcff43d1c351068859aee0edf607c81
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391812"
---
# <a name="rich-text-and-web-services"></a>Rich Text e Serviços Web

O Microsoft InfoPath dá suporte à associação de um controle de **Caixa RTF** em um formulário a um elemento XML que é recebido de um serviço Web e ao envio de dados de um controle de caixa RTF para um elemento XML por meio de um serviço Web. O elemento deve seguir o formato Extensible HTML (XHTML). Por exemplo, o esquema de um elemento chamado `MyRichTextElement` que contém RTF deve ter a seguinte definição de esquema XML: 
  
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

Antes que um controle de **Caixa RTF** possa ser associado com o elemento XHTML, o elemento deve ser encapsulado com um nó de wrapper, que pode pertencer a qualquer namespace arbitrário. O nó de wrapper pode ter esta aparência: 
  
```xml
<xhtmlNode xmlns="https:// someNamespace"> 
    <div xmlns="https://www.w3.org/1999/xhtml">Your rich text here</div> 
</xhtmlNode>
```

Este tópico descreve o processo de criação de um serviço Web que pode enviar e receber XHTML, além de como usar o InfoPath para ligar para os parâmetros de serviço Web. Este tópico fornece instruções detalhadas sobre como criar tal serviço Web. Supomos que você já saiba um pouco sobre como trabalhar com serviços Web.
  
## <a name="how-to-design-a-web-service-to-receive-and-send-xhtml"></a>Como projetar um serviço Web para receber e enviar XHTML

O serviço Web de exemplo armazena dados XHTML que envia e recebe em um arquivo XML no servidor. Esse arquivo é denominado out.xml, e funciona como uma fonte de dados que armazena os dados XHTML. Há dois métodos Web que serão expostos para permitir que um aplicativo cliente comunique com a fonte de dados XHTML: `getXhtml` e `setXhtml`. O método de Serviço Web `getXhtml` retorna um **XmlNode** que contém o XHTML que pode ser associado a um controle de Caixa RTF do InfoPath. O método de Serviço Web `setXhtml` aceita um **XmlNode** como os dados a serem armazenados no arquivo out.xml. 
  
> [!NOTE]
> Esses métodos Web exigem instruções **using** que fazem referência aos namespaces **System.IO** e **System.XML**. 
  
O método de Serviço Web `getXhtml` tenta carregar os dados XML a serem retornados do arquivo out.xml na pasta Data da unidade C. Se ele não conseguir, por o arquivo não ter sido encontrado ou por não conter XML válido, o método retornará um elemento HTML **DIV** vazio que se refere ao namespace XHTML. 
  
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

O método de Serviço Web `setXhtml` aceita XHTML de um controle **Caixa RTF** em um formulário do InfoPath. Como os Serviços Web não têm suporte para uma lista de nós, quando um campo rich text com várias linhas é enviado para um serviço Web, o serviço Web apenas aceita a primeira linha e ignora o restante. 
  
O método `setXhtml` de exemplo supõe que receberá um nó XML de nível superior, que na maioria dos casos estará encapsulado em um elemento **DIV**. Se o XML recebido não contiver um elemento de encapsulamento, como quando o texto dentro do controle de **Caixa RTF** não tem formatação, este método detectará isso verificando se a propriedade **NodeType** indica que o XML passado está em um nó de texto. Se o XML for um nó de texto, o método criará um elemento **DIV** e copiará o conteúdo do nó de texto para o **DIV**, para que o **DIV** contenha um nó de texto filho com o texto que foi enviado para o serviço Web. O XML recebido por esse método é gravado no arquivo out.xml na pasta Data da unidade C. 
  
> [!NOTE]
> O método `setXhtml` de exemplo foi elaborado para aceitar dados XHTML de qualquer tamanho. Na prática, você deve sempre verificar a quantidade de dados que estão sendo enviados e definir um limite máximo para a quantidade de dados que podem ser enviados. 
  
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

## <a name="how-to-create-an-infopath-form-that-exchanges-data-with-the-sample-web-service"></a>Como criar um formulário do InfoPath que troca dados com o serviço Web de exemplo

Execute as etapas a seguir para criar um formulário para testar o serviço Web de exemplo.
  
### <a name="to-create-a-form-that-connects-to-the-sample-web-service"></a>Para criar um formulário que se conecta ao serviço Web exemplo

1. Abra o designer de formulário do InfoPath.
    
2. Na guia **Novo**, clique duas vezes em **Serviço Web** sob **Modelos de Formulário Avançados**.
    
3. Na caixa de diálogo **Assistente de Conexão de Dados**, selecione **Receber dados** e clique em **Avançar**.
    
4. Digite o endereço do serviço Web que contém os métodos de serviço Web de exemplo e clique em **Avançar**. 
    
5. Para o método de recebimento, selecione **getXhtml** como a operação e clique em **Avançar**.
    
6. O método do serviço Web **getXHTML** não recebe parâmetros, portanto clique em **Avançar**.
    
7. Clique em **Concluir**.
    
8. Na guia **Dados**, no grupo **Enviar Ações**, clique em **Para Outros Locais** e clique em **Serviço Web** para usar o mesmo serviço Web para enviar dados. 
    
9. Digite o endereço do serviço Web que contém os métodos de serviço Web de exemplo e clique em **Avançar**.
    
10. Para o método de envio, escolha **setXhtml** como a operação e clique em **Avançar**.
    
11. Clique em **Modificar**, expanda a pasta **dataFields**, expanda a pasta **s0:getXhtmlResponse**, expanda a pasta **getXhtmlResult**, selecione o elemento **MyRichTextElement** e clique em **Avançar**.
    
12. Clique em **Concluir**.
    
13. No painel de tarefas **Campos**, expanda a pasta **dataFields**. 
    
14. Expanda as pastas **s0:getXhtmlResponse** e **getXhtmlResult** e arraste o elemento **MyRichTextElement** para o formulário. O InfoPath reconhecerá que o elemento **MyRichTextElement** é um elemento XHTML e usará um controle de caixa RTF para associar a ele. 
    
15. Salve ou publique o formulário.
    
Para testar o formulário, abra-o, insira algum conteúdo rich text, como imagens, tabelas e texto formatado. Clique em **Enviar** na faixa de opções para armazenar conteúdo rich text no arquivo out.xml no servidor. Clique em **Consulta** na guia **Exibir** e clique no botão **Executar Consulta** no formulário. O controle **Caixa RTF** deverá exibir o conteúdo XHTML do arquivo out.xml. Se o campo rich text contiver várias linhas, o serviço Web somente aceitará a primeira linha e ignorará o restante. 
  

