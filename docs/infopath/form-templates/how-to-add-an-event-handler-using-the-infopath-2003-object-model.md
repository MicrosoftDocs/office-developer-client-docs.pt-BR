---
title: Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath
manager: soliver
ms.date: 01/20/2015
ms.audience: Developer
keywords:
- evento onafterimport [infopath 2007],evento OnAfterChange [InfoPath 2007],evento OnBeforeChange [InfoPath 2007],evento OnSubmitRequest [InfoPath 2007],evento OnVersionUpgrade [InfoPath 2007],modelos de formulário compatíveis com InfoPath 2003, manipulador de eventos,evento OnLoad [InfoPath 2007],manipuladores de eventos [InfoPath 2007], adicionar usando o modelo de objeto do InfoPath 2003,evento OnValidate [InfoPath 2007],evento OnContextChange [InfoPath 2007],evento OnSaveRequest [InfoPath 2007],evento OnClick [InfoPath 2007],evento OnSwitchView [InfoPath 2007],evento OnSign [InfoPath 2007],evento OnMergeRequest [InfoPath 2007]
localization_priority: Normal
ms.assetid: 0520df55-2d91-4cc5-be31-82144a2db4f6
description: Os comandos de menu para adicionar funções de manipulador de eventos em um projeto de modelo de formulário compatível com o modelo de objeto do InfoPath 2003 são essencialmente os mesmos que os dos outros tipos de modelos de formulário.
ms.openlocfilehash: 8533b6bc11dccdad9d0f05de35406ad3cf68eacd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303665"
---
# <a name="add-an-event-handler-using-the-infopath-object-model"></a>Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath

Os comandos de menu para adicionar funções de manipulador de eventos em um projeto de modelo de formulário compatível com o modelo de objeto do InfoPath 2003 são essencialmente os mesmos que os dos outros tipos de modelos de formulário. Por exemplo, para adicionar um manipulador de eventos **OnLoad**, com o modelo de formulário aberto no InfoPath Designer, clique no comando **Evento OnLoad** na guia **Desenvolvedor**. O foco alterna automaticamente para o código de formulário do manipulador de eventos **OnLoad** no editor de código do Visual Studio 2012. 
  
Em projetos de modelo de formulário de código gerenciado compatíveis com o InfoPath 2003, a classe que contém funções de manipulador de eventos e os manipuladores de eventos propriamente ditos são identificados por atributos específicos do InfoPath no módulo de código.

## <a name="adding-event-handlers"></a>Adicionar manipuladores de eventos

Todos os procedimentos a seguir pressupõem que você tenha um projeto de modelo de formulário aberto no Microsoft InfoPath com o Visual Studio 2012.
  
### <a name="add-an-event-handler-for-the-onclick-event-of-a-command-button"></a>Adicionar um manipulador de eventos para o evento OnClick de um botão de comando

1. No painel **Controles**, clique em **Botão** para adicionar um botão ao formulário. 
    
2. Na guia **Propriedades**, clique em **Código personalizado**.
    
   O foco muda para o stub do manipulador de eventos para o evento [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) no editor de código. 
    
### <a name="add-an-event-handler-for-the-onbeforechange-onvalidate-or-onafterchange-event-of-a-field-or-group"></a>Adicionar um manipulador de eventos para o evento OnBeforeChange, OnValidate ou OnAfterChange de um campo ou grupo

1. Clique com o botão direito do mouse em um controle de inserção de dados associado ao campo ou grupo, como um controle **Caixa de Texto**. 
    
2. Aponte para **Programação** e clique em um dos comandos, como **Evento OnValidate**.
    
   O foco alterna para o stub do manipulador de eventos referente a um dos seguintes eventos no editor de código: [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx), [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) ou [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx). 
    
### <a name="add-an-event-handler-for-the-onload-onswitchview-oncontextchange-or-onsign-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento OnLoad, OnSwitchView, OnContextChange ou OnSign de um formulário

- No menu **Ferramentas**, aponte para **Programação** e, em seguida, clique no evento de formulário para o qual você deseja criar um manipulador de eventos.
    
    O foco alterna para o stub do manipulador de eventos referente a um dos seguintes eventos no editor de código: [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx), [OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx), [OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx) ou [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx). 
    
### <a name="add-an-event-handler-for-the-onsubmitrequest-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento OnSubmitRequest de um formulário

1. Na guia **Dados**, clique em **Opções de Envio**.
    
2. Marque a caixa de seleção **Permitir que os usuários enviem este formulário** e clique em **Executar ação personalizada usando Código**.
    
3. Clique em **Editar Código** e, em seguida, clique em **OK**.
    
   O foco muda para o stub do manipulador de eventos do evento [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) no editor de código. 
    
### <a name="add-an-event-handler-for-the-onsaverequest-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento OnSaveRequest de um formulário

1. Clique na guia **Arquivo** e depois em **Opções de Formulário**.
    
2. Na categoria **Salvar**, clique em **Salvar usando código personalizado**, clique em **Editar** e depois em **OK**.
    
   O foco muda para o stub do manipulador de eventos do evento [OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) no editor de código. 
    
### <a name="add-an-event-handler-for-the-onversionupgrade-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento OnVersionUpgrade de um formulário

1. Clique na guia **Arquivo** e depois em **Opções de Formulário**.
    
2. Na categoria **Controle de Versão**, selecione **Usar evento personalizado** na lista **Atualizar formulários existentes**, clique em **Editar** e, em seguida, clique em **OK**.
    
    O foco muda para o stub do manipulador de eventos do evento [OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) no editor de código. 
    
### <a name="add-an-event-handler-for-the-onmergerequest-event-of-a-form"></a>Adicionar um manipulador de eventos para o evento OnMergeRequest de um formulário

1. Clique na guia **Arquivo** e depois em **Opções de Formulário**.
    
2. Na categoria **Avançado**, marque as caixas de seleção **Habilitar mesclagem de formulários** e **Mesclar usando código personalizado**, clique em **Editar** e depois em **OK**.
    
    O foco muda para o stub do manipulador de eventos do evento [OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) no editor de código. 
    
## <a name="adding-an-event-handler-for-the-onafterimport-event"></a>Adicionar um manipulador de eventos para o evento OnAfterImport

Para adicionar manipuladores de eventos para o evento [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx), você deve abrir o código de formulário para o modelo de formulário de código gerenciado e adicionar a função de manipulador de eventos manualmente. Para saber mais sobre como criar um manipulador de eventos para esse evento, clique no link do evento **OnAfterImport**. 
  
## <a name="adding-an-event-handler-for-a-secondary-data-source"></a>Adicionar um manipulador de eventos a uma fonte de dados secundária

O exemplo a seguir mostra como adicionar um manipulador de eventos a uma fonte de dados secundária. O exemplo supõe que existe uma fonte de dados secundária em um arquivo de recursos denominado books.xml, que possui o seguinte esquema:
  
```xml
<?xml version="1.0"?>
<xsd:schema xmlns:xsd="https://www.w3.org/2001/XMLSchema">
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

A exibição do formulário é criada a partir dessa fonte de dados. O código do formulário cria uma tabela de hash com base nos autores e na quantidade de livros que eles escreveram. Você pode atualizar uma entrada da tabela mostrada na exibição, e o manipulador de eventos **OnAfterChange** atualiza a tabela de hash. Observe que a propriedade [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) do atributo **InfoPathEventHandler** (que é implementado pela classe [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx)) é usada para fazer referência à fonte de dados secundária. 
  
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

## <a name="how-the-class-that-contains-event-handlers-is-identified"></a>Como identificar a classe que contém manipuladores de eventos

Ao criar um novo projeto de modelo de formulário do InfoPath compatível com o modelo de objeto de código gerenciado do InfoPath 2003, um atributo **System.ComponentModel.Description** em nível de assembly é aplicado à classe no início do módulo de código de formulário para identificar a classe que contém todos os manipuladores de eventos do modelo de formulário. 
  
> [!IMPORTANT]
> Não modifique o atributo **System.ComponentModel.Description** nessa classe. Se fizer isso, seu modelo de formulário não poderá identificar onde os manipuladores de eventos estão localizados, e estes não serão executados. 
  
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

## <a name="how-event-handlers-are-identified"></a>Como identificar manipuladores de eventos

Ao adicionar um novo manipulador de eventos usando comandos de menu ou botões na interface do usuário do modo de design do InfoPath, o stub para a função do manipulador de eventos é gravado no formulário. O exemplo a seguir mostra o manipulador de eventos do stub criado para um evento [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) adicionado para um campo denominado "Total". 
  
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

Em seguida, você pode adicionar um código que chame membros do modelo de objeto do InfoPath usando os membros em cache particulares das variáveis `thisXDocument` ou `thisApplication`, ou usando os membros acessados ​do objeto `e` **EventArgs** recebidos pelo manipulador de eventos: 
  
```cs
thisXDocument.UI.Alert.(e.Site.text);

```

```vb
thisXDocument.UI.Alert.(e.Site.text)

```

O atributo **InfoPathEventHandler** (conforme definido pela classe [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx)) é o atributo personalizado para funções que serão usadas como manipuladores de eventos. 
  
Quando exigido pelo evento, o parâmetro **MatchPath** (conforme definido pela propriedade [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) da classe **InfoPathEventHandlerAttribute**) especifica uma expressão XPath que identifica a origem do evento. O parâmetro **EventType** (conforme definido pela propriedade [EventType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) da classe **InfoPathEventHandlerAttribute**) especifica o tipo de evento. Você não deve alterar os valores desses parâmetros. Se os valores desses parâmetros forem alterados, o manipulador de eventos pode não ser compilado corretamente, ou a notificação de eventos não ocorrerá conforme esperado. 
  
## <a name="obfuscating-code-in-event-handlers"></a>Ofuscar o código em manipuladores de eventos

Se você executar um utilitário ofuscador no assembly que é gerado ao compilar um modelo de formulário de código gerenciado (*projectname*.dll), o InfoPath não poderá carregar esse assembly quando um usuário abrir o formulário. Se quiser ofuscar o código dos seus manipuladores de eventos ou outro código de formulário, você deverá colocar o código que deseja ofuscar em um assembly separado, fazer referência a esse assembly no seu projeto e, em seguida, chamar membros do assembly mencionado a partir de FormCode.cs ou de FormCode.vb. É importante que você execute o utilitário ofuscador somente no assembly mencionado. 
  
## <a name="see-also"></a>Confira também

- [Responder a eventos de formulário usando o modelo de objeto do InfoPath 2003](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)

