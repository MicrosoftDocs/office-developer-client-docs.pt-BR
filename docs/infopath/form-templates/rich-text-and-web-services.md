---
title: Rich Text e Serviços Web
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
# <a name="rich-text-and-web-services"></a>Rich Text e Serviços Web

Microsoft InfoPath suporta vinculando um controle de **Caixa de Rich Text** em um formulário a um elemento XML que é recebido de um serviço da Web e o envio de dados de um controle de caixa de rich text para um elemento XML por meio de um serviço Web. O elemento deve seguir o formato de linguagem de marcação de hipertexto extensível (XHTML). Por exemplo, o esquema de um elemento chamado `MyRichTextElement` que contém o rich text teria a seguinte definição de esquema XML: 
  
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

Antes de um controle de **Caixa de Rich Text** pode ser vinculado com o elemento XHTML, o elemento deve ser quebrado com um nó de wrapper; Este nó wrapper pode pertencer a qualquer espaço para nome arbitrário. O nó de wrapper pode ter esta aparência: 
  
```xml
<xhtmlNode xmlns="http:// someNamespace"> 
    <div xmlns="http://www.w3.org/1999/xhtml">Your rich text here</div> 
</xhtmlNode>
```

Este tópico descreve o processo de criação de um serviço Web que pode enviar e receber XHTML e como usar o InfoPath para ligar para os parâmetros de serviço Web. Este tópico não fornece instruções detalhadas sobre como criar um serviço Web. Presume-se que você já tem alguma familiaridade com trabalhando com serviços Web.
  
## <a name="how-to-design-a-web-service-to-receive-and-send-xhtml"></a>Como criar um serviço Web para receber e enviar XHTML

O serviço Web de exemplo armazena os dados XHTML que ele envia e recebe em um arquivo XML no servidor. Este arquivo nomeado out.xml, atua como uma fonte de dados que armazena os dados XHTML. Há dois métodos de Web que serão expostos para permitir que um aplicativo cliente para a interface com a fonte de dados XHTML: `getXhtml` e `setXhtml`. O `getXhtml` método de serviço da Web retorna um **XmlNode** que contém o XHTML que pode ser vinculado a um controle de caixa de rich text do InfoPath. O `setXhtml` método de serviço Web aceita um **XmlNode** como os dados para armazenar no arquivo out.xml. 
  
> [!NOTE]
> Estes métodos de Web requerem instruções **using** que fazem referência os namespaces **System.IO** e **System. XML** . 
  
O `getXhtml` método de serviço Web tenta carregar os dados XML a ser retornado do arquivo na pasta Data out.xml na unidade C. Se ele falhar, porque o arquivo não for encontrado ou não contém XML válido, o método retornará um elemento **DIV** HTML vazio que faz referência ao namespace XHTML. 
  
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

O `setXhtml` método de serviço Web aceita XHTML de um controle de **Caixa de Rich Text** em um formulário do InfoPath. Porque os serviços da Web não suportam uma lista de nós, quando um campo de rich text que contém várias linhas é enviado a um serviço Web, o serviço Web apenas aceita a primeira linha e ignora o resto. 
  
O exemplo `setXhtml` método pressupõe que ele receberá um nó XML de nível superior, que, na maioria dos casos, será quebrado em um elemento **DIV** . Se o XML recebido não contiver um elemento de disposição, por exemplo, quando o texto dentro da **Caixa de Rich Text** controlar tem sem formatação, esse método irá detectar isso verificando se a propriedade **NodeType** indica que o XML passado é um nó de texto. Se o XML for um nó de texto, o método cria um elemento **DIV** e copia o conteúdo de nó de texto para a **DIV** , para que as **marcas DIV** contém um filho do nó de texto com o texto que foi enviado para o serviço Web. O XML recebido por esse método é gravado no arquivo out.xml na pasta Data na unidade C. 
  
> [!NOTE]
> O exemplo `setXhtml` método foi escrito para aceitar dados XHTML de qualquer tamanho. Na prática, você sempre deve verificar para ver a quantidade de dados está sendo enviado e definir um limite superior para a quantidade de dados que possa ser enviado. 
  
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

## <a name="how-to-create-an-infopath-form-that-exchanges-data-with-the-sample-web-service"></a>Como criar um formulário do InfoPath que troca de dados com o serviço Web de amostra

Execute as seguintes etapas para criar um formulário para testar o serviço Web de amostra.
  
### <a name="to-create-a-form-that-connects-to-the-sample-web-service"></a>Para criar um formulário que se conecta ao serviço Web de amostra

1. Abra o designer de formulários do InfoPath.
    
2. Na guia **New** , clique duas vezes em **Serviço Web** em **Modelos de formulário avançadas**.
    
3. Na caixa de diálogo **Assistente para Conexão de dados** , selecione a **data de recebimento**e clique em **Avançar**.
    
4. Digite o endereço do serviço da Web que contém os métodos de serviço da Web de amostra e clique em **Avançar**. 
    
5. Para o método de recebimento, selecione **getXhtml** como a operação e clique em **Avançar**.
    
6. **GetXHTML** método Web service não usa nenhum parâmetro, clique em **Avançar**.
    
7. Click **Finish**.
    
8. Na guia **dados** , no grupo **Ações de envio** , clique em **Para outros locais**e clique em **Serviço Web** para usar o mesmo serviço Web para os dados de envio. 
    
9. Digite o endereço do serviço da Web que contém os métodos de serviço da Web de amostra e clique em **Avançar**.
    
10. Para o método de envio, selecione **setXhtml** como a operação e clique em **Avançar**.
    
11. Clique em **Modificar**, expanda a pasta **dataFields** , expanda a pasta **s0:getXhtmlResponse** , expanda a pasta **getXhtmlResult** , selecione o elemento **MyRichTextElement** e clique em **Avançar**.
    
12. Click **Finish**.
    
13. No painel de tarefas **campos** , expanda a pasta de **dataFields** . 
    
14. Expanda as pastas **s0:getXhtmlResponse** e **getXhtmlResult** e, em seguida, arraste o elemento **MyRichTextElement** ao formulário. InfoPath reconhecerá que o elemento **MyRichTextElement** é um elemento XHTML e se usará um controle de caixa de rich text vincular a ela. 
    
15. Salvar ou publicar o formulário.
    
Para testar o formulário, abra o formulário, insira algum conteúdo de rich text como imagens, tabelas e texto formatado. Clique em **Enviar** na faixa de opções para armazenar o conteúdo de rich text no arquivo out.xml no servidor. Clique em **consulta** , na guia **Exibir** e, em seguida, clique no botão **Executar consulta** no formulário. O controle de **Caixa de Rich Text** deve exibir o conteúdo XHTML do arquivo out.xml exe. Se o campo de rich text contiver várias linhas, o serviço da Web apenas aceitar a primeira linha e ignorar o restante. 
  

