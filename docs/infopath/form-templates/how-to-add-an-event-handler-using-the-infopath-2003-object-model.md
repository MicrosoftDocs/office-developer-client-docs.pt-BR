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
# <a name="add-an-event-handler-using-the-infopath-object-model"></a><span data-ttu-id="bb5d3-104">Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath</span><span class="sxs-lookup"><span data-stu-id="bb5d3-104">Add an event handler using the InfoPath object model</span></span>

<span data-ttu-id="bb5d3-105">Os comandos de menu para adicionar funções do manipulador de evento em um projeto de modelo de formulário que seja compatível com o modelo de objeto do InfoPath 2003 são essencialmente os mesmos para outros tipos de modelos de formulário.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-105">The menu commands for adding event handler functions in a form template project that is compatible with the InfoPath 2003 object model are essentially the same as those for other types of form templates.</span></span> <span data-ttu-id="bb5d3-106">Por exemplo, para adicionar um manipulador de eventos **OnLoad** , com o modelo de formulário aberto no InfoPath designer, clique no comando de **Em evento OnLoad** na guia **desenvolvedor** . O foco alterna automaticamente para o código de formulário para o manipulador de evento **OnLoad** no editor de código do Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-106">For example, in order to add an **OnLoad** event handler, with the form template open in the InfoPath designer, click the **On Load Event** command on the **Developer** tab. The focus automatically switches to the form code for the **OnLoad** event handler in the Visual Studio 2012 code editor.</span></span> 
  
<span data-ttu-id="bb5d3-107">Em projetos de modelo de formulário de código gerenciado compatíveis com o InfoPath 2003, a classe que contém funções de manipulador de eventos e os manipuladores de eventos sozinhos são identificadas por atributos específicos do InfoPath no módulo de código.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-107">In managed-code form template projects compatible with InfoPath 2003, the class that contains event handler functions and the event handlers themselves are identified by attributes specific to InfoPath in the code module.</span></span>

## <a name="adding-event-handlers"></a><span data-ttu-id="bb5d3-108">Adicionando manipuladores de eventos</span><span class="sxs-lookup"><span data-stu-id="bb5d3-108">Adding event handlers</span></span>

<span data-ttu-id="bb5d3-109">Todos os procedimentos a seguintes pressupõem que você tenha um projeto de modelo de formulário aberto no Microsoft InfoPath com o Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-109">All of the following procedures assume that you have a form template project open in Microsoft InfoPath with Visual Studio 2012.</span></span>
  
### <a name="add-an-event-handler-for-the-onclick-event-of-a-command-button"></a><span data-ttu-id="bb5d3-110">Adicionar um manipulador de eventos para o evento OnClick de um botão de comando</span><span class="sxs-lookup"><span data-stu-id="bb5d3-110">Add an event handler for the OnClick event of a command button</span></span>

1. <span data-ttu-id="bb5d3-111">No painel de **controles** , clique no **botão** para adicionar um botão ao formulário.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-111">In the **Controls** pane, click **Button** to add a button to the form.</span></span> 
    
2. <span data-ttu-id="bb5d3-112">Na guia **Propriedades** , clique em **Código personalizado**.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-112">On the **Properties** tab, click **Custom Code**.</span></span>
    
   <span data-ttu-id="bb5d3-113">O foco alterna para o fragmento de código para o manipulador de eventos para o evento [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) no editor de código.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-113">The focus switches to the stub for the event handler for the [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onbeforechange-onvalidate-or-onafterchange-event-of-a-field-or-group"></a><span data-ttu-id="bb5d3-114">Adicionar um manipulador de eventos para o evento OnBeforeChange, OnValidate ou OnAfterChange de um campo ou grupo</span><span class="sxs-lookup"><span data-stu-id="bb5d3-114">Add an event handler for the OnBeforeChange, OnValidate, or OnAfterChange event of a field or group</span></span>

1. <span data-ttu-id="bb5d3-115">Clique com o botão um controle de entrada de dados vinculado ao campo ou grupo, como um controle de **Caixa de texto** .</span><span class="sxs-lookup"><span data-stu-id="bb5d3-115">Right-click a data-entry control bound to the field or group, such as a **Text Box** control.</span></span> 
    
2. <span data-ttu-id="bb5d3-116">Aponte para **programação**e clique em um dos comandos, como **No evento validar**.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-116">Point to **Programming**, and then click one of the commands, such as **On Validate Event**.</span></span>
    
   <span data-ttu-id="bb5d3-117">O foco alterna para o fragmento de código para o manipulador de eventos para um dos seguintes eventos no editor de código: [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx), [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx)ou [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx).</span><span class="sxs-lookup"><span data-stu-id="bb5d3-117">The focus switches to the stub for the event handler for one of the following events in the code editor: [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx), [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx), or [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx).</span></span> 
    
### <a name="add-an-event-handler-for-the-onload-onswitchview-oncontextchange-or-onsign-event-of-a-form"></a><span data-ttu-id="bb5d3-118">Adicionar um manipulador de eventos para o evento OnLoad, OnSwitchView, OnContextChange ou OnSign de um formulário</span><span class="sxs-lookup"><span data-stu-id="bb5d3-118">Add an event handler for the OnLoad, OnSwitchView, OnContextChange, or OnSign event of a form</span></span>

- <span data-ttu-id="bb5d3-119">No menu **Ferramentas** , aponte para **programação**e clique no evento de formulário que você deseja gravar um manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-119">On the **Tools** menu, point to **Programming**, and then click the form event that you want to write an event handler for.</span></span>
    
    <span data-ttu-id="bb5d3-120">O foco alterna para o fragmento de código para o manipulador de eventos para um dos seguintes no editor de código: [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx), [OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx), [OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx)ou [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx).</span><span class="sxs-lookup"><span data-stu-id="bb5d3-120">The focus switches to the stub for the event handler for one of the following in the code editor: [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx), [OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx), [OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx), or [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx).</span></span> 
    
### <a name="add-an-event-handler-for-the-onsubmitrequest-event-of-a-form"></a><span data-ttu-id="bb5d3-121">Adicionar um manipulador de eventos para o evento OnSubmitRequest de um formulário</span><span class="sxs-lookup"><span data-stu-id="bb5d3-121">Add an event handler for the OnSubmitRequest event of a form</span></span>

1. <span data-ttu-id="bb5d3-122">Na guia **dados** , clique em **Opções de envio**.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-122">On the **Data** tab, click **Submit Options**.</span></span>
    
2. <span data-ttu-id="bb5d3-123">Marque a caixa de seleção **Permitir que os usuários enviem este formulário** e clique em **Executar ação personalizada usando o código**.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-123">Select the **Allow users to submit this form** check box, and then click **Perform custom action using Code**.</span></span>
    
3. <span data-ttu-id="bb5d3-124">Clique em **Editar código**e clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-124">Click **Edit Code**, and then click **OK**.</span></span>
    
   <span data-ttu-id="bb5d3-125">O foco alterna para o fragmento de código para o manipulador de eventos para o evento [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) no editor de código.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-125">The focus switches to the stub for the event handler for the [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onsaverequest-event-of-a-form"></a><span data-ttu-id="bb5d3-126">Adicionar um manipulador de eventos para o evento OnSaveRequest de um formulário</span><span class="sxs-lookup"><span data-stu-id="bb5d3-126">Add an event handler for the OnSaveRequest event of a form</span></span>

1. <span data-ttu-id="bb5d3-127">Clique na guia **arquivo** e, em seguida, clique em **Opções de formulário**.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-127">Click the **File** tab, and then click **Form Options**.</span></span>
    
2. <span data-ttu-id="bb5d3-128">Na categoria **Salvar** , clique em **Salvar usando código personalizado**, clique em **Editar**e, em seguida, clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-128">In the **Save** category, click **Save using custom code**, click **Edit**, and then click **OK**.</span></span>
    
   <span data-ttu-id="bb5d3-129">O foco alterna para o fragmento de código para o manipulador de eventos para o evento [OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) no editor de código.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-129">The focus switches to the stub for the event handler for the [OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onversionupgrade-event-of-a-form"></a><span data-ttu-id="bb5d3-130">Adicionar um manipulador de eventos para o evento OnVersionUpgrade de um formulário</span><span class="sxs-lookup"><span data-stu-id="bb5d3-130">Add an event handler for the OnVersionUpgrade event of a form</span></span>

1. <span data-ttu-id="bb5d3-131">Clique na guia **arquivo** e, em seguida, clique em **Opções de formulário**.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-131">Click the **File** tab, and then click **Form Options**.</span></span>
    
2. <span data-ttu-id="bb5d3-132">Na categoria **controle de versão** , selecione o **evento de uso personalizado** na lista **Atualizar formulários existentes** , clique em **Editar**e, em seguida, clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-132">In the **Versioning** category, select **Use custom event** from the **Update existing forms** list, click **Edit**, and then click **OK**.</span></span>
    
    <span data-ttu-id="bb5d3-133">O foco alterna para o fragmento de código para o manipulador de eventos para o evento [OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) no editor de código.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-133">The focus switches to the stub for the event handler for the [OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onmergerequest-event-of-a-form"></a><span data-ttu-id="bb5d3-134">Adicionar um manipulador de eventos para o evento OnMergeRequest de um formulário</span><span class="sxs-lookup"><span data-stu-id="bb5d3-134">Add an event handler for the OnMergeRequest event of a form</span></span>

1. <span data-ttu-id="bb5d3-135">Clique na guia **arquivo** e, em seguida, clique em **Opções de formulário**.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-135">Click the **File** tab, and then click **Form Options**.</span></span>
    
2. <span data-ttu-id="bb5d3-136">Na categoria **Avançado** , selecione a **mesclagem de formulários habilitar** e as caixas de seleção **Mesclar usando código personalizado** , clique em **Editar**e, em seguida, clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-136">In the **Advanced** category, select the **Enable Form merging** and the **Merge using custom code** check boxes, click **Edit**, and then click **OK**.</span></span>
    
    <span data-ttu-id="bb5d3-137">O foco alterna para o fragmento de código para o manipulador de eventos para o evento [OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) no editor de código.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-137">The focus switches to the stub for the event handler for the [OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) event in the code editor.</span></span> 
    
## <a name="adding-an-event-handler-for-the-onafterimport-event"></a><span data-ttu-id="bb5d3-138">Adicionando um manipulador de eventos para o evento OnAfterImport</span><span class="sxs-lookup"><span data-stu-id="bb5d3-138">Adding an event handler for the OnAfterImport event</span></span>

<span data-ttu-id="bb5d3-139">Para adicionar manipuladores de eventos para o evento [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) , você deve abrir o código de formulário para o seu modelo de formulário de código gerenciado e adicionar a função do manipulador de eventos manualmente.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-139">To add event handlers for the [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) event, you must open the form code for your managed-code form template and add the event handler function manually.</span></span> <span data-ttu-id="bb5d3-140">Para obter informações sobre como escrever um manipulador de eventos para este evento, clique no link para o evento **OnAfterImport** .</span><span class="sxs-lookup"><span data-stu-id="bb5d3-140">For information on how to write an event handler for this event, click the link for the **OnAfterImport** event.</span></span> 
  
## <a name="adding-an-event-handler-for-a-secondary-data-source"></a><span data-ttu-id="bb5d3-141">Adicionando um manipulador de eventos para uma fonte de dados secundário</span><span class="sxs-lookup"><span data-stu-id="bb5d3-141">Adding an event handler for a secondary data source</span></span>

<span data-ttu-id="bb5d3-142">O exemplo a seguir mostra como adicionar um manipulador de eventos para uma fonte de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-142">The following example shows how to add an event handler for a secondary data source.</span></span> <span data-ttu-id="bb5d3-143">O exemplo supõe que uma fonte de dados secundário de um arquivo de recurso chamado Books. XML, que tem o esquema a seguir:</span><span class="sxs-lookup"><span data-stu-id="bb5d3-143">The example assumes a secondary data source from a resource file named books.xml, which has the following schema:</span></span>
  
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

<span data-ttu-id="bb5d3-144">Modo de exibição do formulário é construído a partir dessa fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-144">The form's view is built from this data source.</span></span> <span data-ttu-id="bb5d3-145">O código do formulário cria uma tabela de hash com base nos autores e o número de livros que ele tenham escrito.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-145">The form code creates a hash table based on the authors and the number of books they have written.</span></span> <span data-ttu-id="bb5d3-146">Você pode atualizar uma entrada da tabela mostrada no modo de exibição e o manipulador de eventos **OnAfterChange** atualiza a tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-146">You can update an entry from the table shown in the view and the **OnAfterChange** event handler updates the hash table.</span></span> <span data-ttu-id="bb5d3-147">Observe que a propriedade [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) do atributo **InfoPathEventHandler** (que é implementado pela classe [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) é usada para fazer referência a fonte de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-147">Note that the [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) property of the **InfoPathEventHandler** attribute (which is implemented by the [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) class) is used to reference the secondary data source.</span></span> 
  
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

## <a name="how-the-class-that-contains-event-handlers-is-identified"></a><span data-ttu-id="bb5d3-148">Como a classe que contém manipuladores de eventos é identificada</span><span class="sxs-lookup"><span data-stu-id="bb5d3-148">How the class that contains event handlers is identified</span></span>

<span data-ttu-id="bb5d3-149">Quando você cria um novo projeto de modelo de formulário do InfoPath que seja compatível com o modelo de objeto de código gerenciado do InfoPath 2003, um atributo de **System.ComponentModel.Description** de nível de assembly é aplicado à classe no início do módulo de código do formulário para identifica a classe que contém todos os manipuladores de eventos para o modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-149">When you create a new InfoPath form template project that is compatible with the InfoPath 2003 managed code object model, an assembly-level **System.ComponentModel.Description** attribute is applied to the class at the beginning of the form code module to identify the class that contains all event handlers for the form template.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="bb5d3-150">Não modifique o atributo **System.ComponentModel.Description** nesta classe.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-150">Do not modify the **System.ComponentModel.Description** attribute in this class.</span></span> <span data-ttu-id="bb5d3-151">Se fizer isso, o seu modelo de formulário não será capaz de identificar onde manipuladores de eventos estão localizados e os manipuladores de eventos não funcionará.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-151">If you do so, your form template will not be able to identify where event handlers are located, and the event handlers will fail to run.</span></span> 
  
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

## <a name="how-event-handlers-are-identified"></a><span data-ttu-id="bb5d3-152">Como os manipuladores de eventos são identificados</span><span class="sxs-lookup"><span data-stu-id="bb5d3-152">How event handlers are identified</span></span>

<span data-ttu-id="bb5d3-153">Quando você adiciona um novo manipulador de eventos usando comandos de menu ou botões na interface de usuário do modo de design do InfoPath, o fragmento de código para a função do manipulador de eventos é gravado no formulário.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-153">When you add a new event handler using menu commands or buttons in the InfoPath design mode user interface, the stub for the event handler function is written into the form.</span></span> <span data-ttu-id="bb5d3-154">O exemplo a seguir mostra o manipulador de eventos stub criado para um [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) adicionados para um campo denominado 'total'.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-154">The following example shows the stub event handler created for an [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) added for a field named 'total'.</span></span> 
  
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

<span data-ttu-id="bb5d3-155">Você pode adicionar código que invoca membros do modelo de objeto do InfoPath usando os membros de cache privados do `thisXDocument` ou `thisApplication` variáveis, ou usando os membros acessados a partir o `e` objeto **EventArgs** recebido pelo manipulador de eventos:</span><span class="sxs-lookup"><span data-stu-id="bb5d3-155">You can then add code that invokes members of the InfoPath object model using the private cached members of the  `thisXDocument` or  `thisApplication` variables, or by using the members accessed from the  `e` **EventArgs** object received by the event handler:</span></span> 
  
```cs
thisXDocument.UI.Alert.(e.Site.text);

```

```vb
thisXDocument.UI.Alert.(e.Site.text)

```

<span data-ttu-id="bb5d3-156">O atributo **InfoPathEventHandler** (conforme definido pela classe [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) é o atributo personalizado para funções que será usado como manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-156">The **InfoPathEventHandler** attribute (as defined by the [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) class) is the custom attribute for functions that will be used as event handlers.</span></span> 
  
<span data-ttu-id="bb5d3-157">Quando solicitado pelo evento, o parâmetro **MatchPath** (conforme definido pela propriedade [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) da classe **InfoPathEventHandlerAttribute** ) especifica uma expressão XPath que identifica a origem do evento.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-157">When required by the event, the **MatchPath** parameter (as defined by the [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) property of the **InfoPathEventHandlerAttribute** class) specifies an XPath expression that identifies the event source.</span></span> <span data-ttu-id="bb5d3-158">O parâmetro **EventType** (conforme definido pela propriedade [EventType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) da classe **InfoPathEventHandlerAttribute** ) Especifica o tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-158">The **EventType** parameter (as defined by the [EventType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) property of the **InfoPathEventHandlerAttribute** class) specifies the type of event.</span></span> <span data-ttu-id="bb5d3-159">Você não deve alterar os valores desses parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-159">You should not change the values of these parameters.</span></span> <span data-ttu-id="bb5d3-160">Se os valores desses parâmetros forem alterados, o manipulador de eventos não pode compilar corretamente ou notificação de evento não ocorrerá conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-160">If the values of these parameters are changed, the event handler may not compile correctly, or event notification will not occur as expected.</span></span> 
  
## <a name="obfuscating-code-in-event-handlers"></a><span data-ttu-id="bb5d3-161">Código de ofuscação nos manipuladores de eventos</span><span class="sxs-lookup"><span data-stu-id="bb5d3-161">Obfuscating code in event handlers</span></span>

<span data-ttu-id="bb5d3-162">Se você executar um utilitário ofuscador no assembly gerado quando um modelo de formulário de código gerenciado é compilado ( *NomeDoProjeto* . dll), o InfoPath não será possível carregar o assembly quando um usuário abre o formulário.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-162">If you run an obfuscator utility on the assembly that is generated when a managed-code form template is compiled ( *projectname*  .dll), InfoPath will not be able to load the assembly when a user opens the form.</span></span> <span data-ttu-id="bb5d3-163">Se você quiser obscurecer o código para os manipuladores de eventos ou outro código de formulário, você deve colocar o código que você deseja obscurecer em um assembly separado e referência de assembly em seu projeto e, em seguida, chamam membros do assembly referenciado de FormCode.cs ou FormCode.vb.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-163">If you want to obfuscate the code for your event handlers or other form code, you must put the code that you want to obfuscate in a separate assembly, and reference that assembly in your project, and then call members of the referenced assembly from FormCode.cs or FormCode.vb.</span></span> <span data-ttu-id="bb5d3-164">É importante que você execute o utilitário ofuscador apenas no assembly referenciado.</span><span class="sxs-lookup"><span data-stu-id="bb5d3-164">It is important that you run the obfuscator utility only on the referenced assembly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bb5d3-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb5d3-165">See also</span></span>

- [<span data-ttu-id="bb5d3-166">Responder para formar eventos usando o modelo de objeto do InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="bb5d3-166">Respond to Form Events Using the InfoPath 2003 Object Model</span></span>](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)

