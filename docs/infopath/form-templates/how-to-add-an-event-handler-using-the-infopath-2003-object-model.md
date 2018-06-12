---
title: Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath
manager: soliver
ms.date: 01/20/2015
ms.audience: Developer
keywords:
- evento OnAfterImport [infopath 2007], evento OnAfterChange [InfoPath 2007], evento OnBeforeChange [InfoPath 2007], evento OnSubmitRequest [InfoPath 2007], evento OnVersionUpgrade [InfoPath 2007], modelos de formulário compatíveis com o InfoPath 2003, manipuladores de eventos Evento onLoad [InfoPath 2007], [InfoPath 2007], manipuladores de eventos adicionando usando o modelo de objeto do InfoPath 2003, evento OnValidate [InfoPath 2007], o evento OnContextChange [InfoPath 2007], o evento OnSaveRequest [InfoPath 2007], o evento OnClick [InfoPath 2007] Evento de OnSwitchView [InfoPath 2007], evento OnSign [InfoPath 2007], evento OnMergeRequest [InfoPath 2007]
localization_priority: Normal
ms.assetid: 0520df55-2d91-4cc5-be31-82144a2db4f6
description: Os comandos de menu para adicionar funções do manipulador de evento em um projeto de modelo de formulário que seja compatível com o modelo de objeto do InfoPath 2003 são essencialmente os mesmos para outros tipos de modelos de formulário.
ms.openlocfilehash: 9f037c59180b9c8d858ec73d79ef892974efe483
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765618"
---
# <a name="add-an-event-handler-using-the-infopath-object-model"></a>Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath

Os comandos de menu para adicionar funções do manipulador de evento em um projeto de modelo de formulário que seja compatível com o modelo de objeto do InfoPath 2003 são essencialmente os mesmos para outros tipos de modelos de formulário. Por exemplo, para adicionar um manipulador de eventos **OnLoad** , com o modelo de formulário aberto no InfoPath designer, clique no comando de **Em evento OnLoad** na guia **desenvolvedor** . O foco alterna automaticamente para o código de formulário para o manipulador de evento **OnLoad** no editor de código do Visual Studio 2012. 
  
Em projetos de modelo de formulário de código gerenciado compatíveis com o InfoPath 2003, a classe que contém funções de manipulador de eventos e os manipuladores de eventos sozinhos são identificadas por atributos específicos do InfoPath no módulo de código.

## <a name="adding-event-handlers"></a>Adicionando manipuladores de eventos

Todos os procedimentos a seguintes pressupõem que você tenha um projeto de modelo de formulário aberto no Microsoft InfoPath com o Visual Studio 2012.
  
### <a name="add-an-event-handler-for-the-onclick-event-of-a-command-button"></a>Adicionar um manipulador de eventos para o evento OnClick de um botão de comando

1. No painel de **controles** , clique no **botão** para adicionar um botão ao formulário. 
    
2. Na guia **Propriedades** , clique em **Código personalizado**.
    
   O foco alterna para o fragmento de código para o manipulador de eventos para o evento [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) no editor de código. 
    
### <a name="add-an-event-handler-for-the-onbeforechange-onvalidate-or-onafterchange-event-of-a-field-or-group"></a>Adicionar um manipulador de eventos para o evento OnBeforeChange, OnValidate ou OnAfterChange de um campo ou grupo

1. Clique com o botão um controle de entrada de dados vinculado ao campo ou grupo, como um controle de **Caixa de texto** . 
    
2. Aponte para **programação**e clique em um dos comandos, como **No evento validar**.
    
   O foco alterna para o fragmento de código para o manipulador de eventos para um dos seguintes eventos no editor de código: [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx), [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx)ou [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx). 
    
### <a name="add-an-event-handler-for-the-onload-onswitchview-oncontextchange-or-onsign-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento OnLoad, OnSwitchView, OnContextChange ou OnSign de um formulário

- No menu **Ferramentas** , aponte para **programação**e clique no evento de formulário que você deseja gravar um manipulador de eventos.
    
    O foco alterna para o fragmento de código para o manipulador de eventos para um dos seguintes no editor de código: [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx), [OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx), [OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx)ou [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx). 
    
### <a name="add-an-event-handler-for-the-onsubmitrequest-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento OnSubmitRequest de um formulário

1. Na guia **dados** , clique em **Opções de envio**.
    
2. Marque a caixa de seleção **Permitir que os usuários enviem este formulário** e clique em **Executar ação personalizada usando o código**.
    
3. Clique em **Editar código**e clique em **Okey**.
    
   O foco alterna para o fragmento de código para o manipulador de eventos para o evento [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) no editor de código. 
    
### <a name="add-an-event-handler-for-the-onsaverequest-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento OnSaveRequest de um formulário

1. Clique na guia **arquivo** e, em seguida, clique em **Opções de formulário**.
    
2. Na categoria **Salvar** , clique em **Salvar usando código personalizado**, clique em **Editar**e, em seguida, clique em **Okey**.
    
   O foco alterna para o fragmento de código para o manipulador de eventos para o evento [OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) no editor de código. 
    
### <a name="add-an-event-handler-for-the-onversionupgrade-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento OnVersionUpgrade de um formulário

1. Clique na guia **arquivo** e, em seguida, clique em **Opções de formulário**.
    
2. Na categoria **controle de versão** , selecione o **evento de uso personalizado** na lista **Atualizar formulários existentes** , clique em **Editar**e, em seguida, clique em **Okey**.
    
    O foco alterna para o fragmento de código para o manipulador de eventos para o evento [OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) no editor de código. 
    
### <a name="add-an-event-handler-for-the-onmergerequest-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento OnMergeRequest de um formulário

1. Clique na guia **arquivo** e, em seguida, clique em **Opções de formulário**.
    
2. Na categoria **Avançado** , selecione a **mesclagem de formulários habilitar** e as caixas de seleção **Mesclar usando código personalizado** , clique em **Editar**e, em seguida, clique em **Okey**.
    
    O foco alterna para o fragmento de código para o manipulador de eventos para o evento [OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) no editor de código. 
    
## <a name="adding-an-event-handler-for-the-onafterimport-event"></a>Adicionando um manipulador de eventos para o evento OnAfterImport

Para adicionar manipuladores de eventos para o evento [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) , você deve abrir o código de formulário para o seu modelo de formulário de código gerenciado e adicionar a função do manipulador de eventos manualmente. Para obter informações sobre como escrever um manipulador de eventos para este evento, clique no link para o evento **OnAfterImport** . 
  
## <a name="adding-an-event-handler-for-a-secondary-data-source"></a>Adicionando um manipulador de eventos para uma fonte de dados secundário

O exemplo a seguir mostra como adicionar um manipulador de eventos para uma fonte de dados secundário. O exemplo supõe que uma fonte de dados secundário de um arquivo de recurso chamado Books. XML, que tem o esquema a seguir:
  
```xml
<?xml version="1.0"?>
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <xsd:element name="catalog">
        <xsd:complexType>
            <xsd:sequence>
                <xsd:element ref="book" minOccurs="0" maxOccurs="unbounded"></xsd:element>
            </xsd:sequence>
        </xsd:complexType>
    </xsd:element>
    <xsd:element name="genre" type="xsd:string"></xsd:element>
    <xsd:element name="author" type="xsd:string"></xsd:element>
    <xsd:element name="book">
        <xsd:complexType>
            <xsd:all>
                <xsd:element ref="author" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="title" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="genre" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="price" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="publish_date" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="description" minOccurs="0" maxOccurs="1"></xsd:element>
            </xsd:all>
            <xsd:attribute ref="id"></xsd:attribute>
        </xsd:complexType>
    </xsd:element>
    <xsd:element name="price" type="xsd:string"></xsd:element>
    <xsd:element name="title" type="xsd:string"></xsd:element>
    <xsd:element name="publish_date" type="xsd:string"></xsd:element>
    <xsd:element name="description" type="xsd:string"></xsd:element>
    <xsd:attribute name="id" type="xsd:string"></xsd:attribute>
</xsd:schema>

```

<br/>

Modo de exibição do formulário é construído a partir dessa fonte de dados. O código do formulário cria uma tabela de hash com base nos autores e o número de livros que ele tenham escrito. Você pode atualizar uma entrada da tabela mostrada no modo de exibição e o manipulador de eventos **OnAfterChange** atualiza a tabela de hash. Observe que a propriedade [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) do atributo **InfoPathEventHandler** (que é implementado pela classe [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) é usada para fazer referência a fonte de dados secundário. 
  
```cs
namespace AuxDom
{
    // InfoPathNamespace attribute goes here.
    public class AuxDom
    {
        private XDocument thisXDocument;
        private Application thisApplication;
        private Hashtable authors;
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            authors = new Hashtable();
        }
        public void _Shutdown()
        {
            authors.Clear();
        }
        // The following function handler is created by Microsoft
        // Office InfoPath. Do not modify the type or number of
        // arguments. 
        [InfoPathEventHandler(EventType=InfoPathEventType.OnLoad)]
        public void OnLoad(DocReturnEvent e)
        {
            IXMLDOMDocument books = thisXDocument.GetDOM("books");
            DOMNodeList externalAuthors = books.selectNodes("/catalog/book/author");
            foreach (IXMLDOMNode authorNode in externalAuthors)
            {
                AddBookFromAuthor(authorNode.text);
            }
        }
        // The following function handler is created by Microsoft
        // Office InfoPath. Do not modify the type or number of
        // arguments. 
        [InfoPathEventHandler(MatchPath="/catalog/book/author", EventType=InfoPathEventType.OnAfterChange, DataObject="books")]
        public void books__author_OnAfterChange(DataDOMEvent e)
        {
            if (e.IsUndoRedo)
            {
                // An undo or redo operation has occurred and the DOM 
                // is read-only.
                return;
            }
            
            if (e.Source.text != e.NewValue.ToString())
            {
                RemoveBookFromAuthor(e.OldValue.ToString());
                AddBookFromAuthor(e.NewValue.ToString());
            }
        }
        private void AddBookFromAuthor(string authorName)
        {
            if (authors.Contains(authorName))
            {
                authors[authorName] = (int)authors[authorName] + 1;
            }
            else
            {
                authors.Add(authorName, 1);
            }
        }
        private void RemoveBookFromAuthor(string authorName)
        {
            if (authors.Contains(authorName))
            {
                authors[authorName] = (int)authors[authorName] - 1;
            }
            if ((int)authors[authorName] == 0)
            {
                authors.Remove(authorName);
            }
        }
        // The following function handler is created by Microsoft
        // Office InfoPath. Do not modify the type or number of
        // arguments. 
        [InfoPathEventHandler(MatchPath="ShowAuthors", EventType=InfoPathEventType.OnClick)]
        public void ShowAuthors_OnClick(DocActionEvent e)
        {
            // Write your code here.
            StringBuilder report = new StringBuilder();
            foreach (string authorName in authors.Keys)
            {
                report.Append(authorName + ",\t\t\t");
                report.Append(authors[authorName] + "\n");
            }
            thisXDocument.UI.Alert(report.ToString());
        }
    }
}

```

## <a name="how-the-class-that-contains-event-handlers-is-identified"></a>Como a classe que contém manipuladores de eventos é identificada

Quando você cria um novo projeto de modelo de formulário do InfoPath que seja compatível com o modelo de objeto de código gerenciado do InfoPath 2003, um atributo de **System.ComponentModel.Description** de nível de assembly é aplicado à classe no início do módulo de código do formulário para identifica a classe que contém todos os manipuladores de eventos para o modelo de formulário. 
  
> [!IMPORTANT]
> Não modifique o atributo **System.ComponentModel.Description** nesta classe. Se fizer isso, o seu modelo de formulário não será capaz de identificar onde manipuladores de eventos estão localizados e os manipuladores de eventos não funcionará. 
  
```cs
using System;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
// Office integration attribute. Identifies the startup class for the // form. Do not modify.
[assembly: System.ComponentModel.DescriptionAttribute(    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")]
```

```vb
Imports System
Imports Microsoft.Office.Interop.InfoPath.SemiTrust
' Office integration attribute. Identifies the startup class for the form. Do not modify.
<Assembly: System.ComponentModel.DescriptionAttribute( _    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")>
```

## <a name="how-event-handlers-are-identified"></a>Como os manipuladores de eventos são identificados

Quando você adiciona um novo manipulador de eventos usando comandos de menu ou botões na interface de usuário do modo de design do InfoPath, o fragmento de código para a função do manipulador de eventos é gravado no formulário. O exemplo a seguir mostra o manipulador de eventos stub criado para um [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) adicionados para um campo denominado 'total'. 
  
```cs
[InfoPathEventHandler(MatchPath="/invoice/total", EventType=InfoPathEventType.OnValidate)]
public void total_OnValidate(DataDOMEvent e)
{
    // Write your code here.
}

```

```vb
<InfoPathEventHandler(MatchPath:="/invoice/total",EventType:= OnValidate)> Public Sub total_OnValidate(ByVal e As EventArgs)
    ' Write your code here.
End Sub

```

Você pode adicionar código que invoca membros do modelo de objeto do InfoPath usando os membros de cache privados do `thisXDocument` ou `thisApplication` variáveis, ou usando os membros acessados a partir o `e` objeto **EventArgs** recebido pelo manipulador de eventos: 
  
```cs
thisXDocument.UI.Alert.(e.Site.text);

```

```vb
thisXDocument.UI.Alert.(e.Site.text)

```

O atributo **InfoPathEventHandler** (conforme definido pela classe [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) é o atributo personalizado para funções que será usado como manipuladores de eventos. 
  
Quando solicitado pelo evento, o parâmetro **MatchPath** (conforme definido pela propriedade [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) da classe **InfoPathEventHandlerAttribute** ) especifica uma expressão XPath que identifica a origem do evento. O parâmetro **EventType** (conforme definido pela propriedade [EventType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) da classe **InfoPathEventHandlerAttribute** ) Especifica o tipo de evento. Você não deve alterar os valores desses parâmetros. Se os valores desses parâmetros forem alterados, o manipulador de eventos não pode compilar corretamente ou notificação de evento não ocorrerá conforme o esperado. 
  
## <a name="obfuscating-code-in-event-handlers"></a>Código de ofuscação nos manipuladores de eventos

Se você executar um utilitário ofuscador no assembly gerado quando um modelo de formulário de código gerenciado é compilado ( *NomeDoProjeto* . dll), o InfoPath não será possível carregar o assembly quando um usuário abre o formulário. Se você quiser obscurecer o código para os manipuladores de eventos ou outro código de formulário, você deve colocar o código que você deseja obscurecer em um assembly separado e referência de assembly em seu projeto e, em seguida, chamam membros do assembly referenciado de FormCode.cs ou FormCode.vb. É importante que você execute o utilitário ofuscador apenas no assembly referenciado. 
  
## <a name="see-also"></a>Confira também

- [Responder para formar eventos usando o modelo de objeto do InfoPath 2003](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)

