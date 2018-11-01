---
title: Salve o método - ActiveX Data Objects (ADO)
TOCTitle: Save Method (ADO)
ms:assetid: 02dab13b-f947-b96d-46ea-0def3ed8f28f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248793(v=office.15)
ms:contentKeyID: 48542968
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b4e3698043c109a8f0fbf32c5c2b8c8ae20e824
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875977"
---
# <a name="save-method-ado"></a><span data-ttu-id="881dc-102">Método Save (ADO)</span><span class="sxs-lookup"><span data-stu-id="881dc-102">Save Method (ADO)</span></span>


<span data-ttu-id="881dc-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="881dc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="881dc-104">Salva o [Recordset](recordset-object-ado.md) em um arquivo ou objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="881dc-104">Saves the [Recordset](recordset-object-ado.md) in a file or [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="881dc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="881dc-105">Syntax</span></span>

<span data-ttu-id="881dc-106">*conjunto de registros*. Salvar*destino*, *PersistFormat*</span><span class="sxs-lookup"><span data-stu-id="881dc-106">*recordset*.Save*Destination*, *PersistFormat*</span></span>

## <a name="parameters"></a><span data-ttu-id="881dc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="881dc-107">Parameters</span></span>

  - <span data-ttu-id="881dc-108">*Destination*</span><span class="sxs-lookup"><span data-stu-id="881dc-108">*Destination*</span></span>

  - <span data-ttu-id="881dc-p101">Opcional. Uma **Variant** que representa o nome de caminho completo do arquivo em que o **Recordset** deve ser salvo, ou uma referência a um objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="881dc-p101">Optional. A **Variant** that represents the complete path name of the file where the **Recordset** is to be saved, or a reference to a **Stream** object.</span></span>

  - <span data-ttu-id="881dc-111">*PersistFormat*</span><span class="sxs-lookup"><span data-stu-id="881dc-111">*PersistFormat*</span></span>

  - <span data-ttu-id="881dc-p102">Opcional. Um valor [PersistFormatEnum](persistformatenum.md) que especifica o formato no qual o **Recordset** deve ser salvo (XML ou ADTG). O valor padrão é **adPersistADTG**.</span><span class="sxs-lookup"><span data-stu-id="881dc-p102">Optional. A [PersistFormatEnum](persistformatenum.md) value that specifies the format in which the **Recordset** is to be saved (XML or ADTG). The default value is **adPersistADTG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="881dc-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="881dc-115">Remarks</span></span>

<span data-ttu-id="881dc-p103">O método **Save** pode ser chamado apenas em um **Recordset** aberto. Utilize o método [Open](open-method-ado-recordset.md) para posteriormente restaurar o **Recordset** do *Destination*.</span><span class="sxs-lookup"><span data-stu-id="881dc-p103">The **Save** method can only be invoked on an open **Recordset**. Use the [Open](open-method-ado-recordset.md) method to later restore the **Recordset** from *Destination*.</span></span>

<span data-ttu-id="881dc-p104">Se a propriedade [Filter](filter-property-ado.md) estiver em efeito para o **Recordset**, apenas as linhas acessíveis sob o filtro serão salvas. Se o **Recordset** for hierárquico, o **Recordset** filho atual e seus filhos serão salvos, incluindo o **Recordset** pai. Se o método **Save** de um **Recordset** filho for chamado, o filho e seus filhos serão salvos, mas o pai não o será.</span><span class="sxs-lookup"><span data-stu-id="881dc-p104">If the [Filter](filter-property-ado.md) property is in effect for the **Recordset**, then only the rows accessible under the filter are saved. If the **Recordset** is hierarchical, then the current child **Recordset** and its children are saved, including the parent **Recordset**. If the **Save** method of a child **Recordset** is called, the child and all its children are saved, but the parent is not.</span></span>

<span data-ttu-id="881dc-p105">Na primeira vez que você salva o **Recordset**, é opcional especificar *Destination*. Se você omitir *Destination*, será criado um novo arquivo com o nome definido como o valor da propriedade [Source](source-property-ado-recordset.md) do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="881dc-p105">The first time you save the **Recordset**, it is optional to specify *Destination*. If you omit *Destination*, a new file will be created with a name set to the value of the [Source](source-property-ado-recordset.md) property of the **Recordset**.</span></span>

<span data-ttu-id="881dc-123">Omita *destino* quando você chama subsequentemente **Salvar** após o primeiro salvar ou ocorrerá um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="881dc-123">Omit *Destination* when you subsequently call **Save** after the first save, or a run-time error will occur.</span></span> <span data-ttu-id="881dc-124">Se você subsequentemente chamar **Salvar** com um novo *destino*, o **Recordset** é salvo para o novo destino.</span><span class="sxs-lookup"><span data-stu-id="881dc-124">If you subsequently call **Save** with a new *Destination*, the **Recordset** is saved to the new destination.</span></span> <span data-ttu-id="881dc-125">No entanto, o novo destino e o destino original estarão ambos abertos.</span><span class="sxs-lookup"><span data-stu-id="881dc-125">However, the new destination and the original destination will both be open.</span></span>

<span data-ttu-id="881dc-p107">**Save** não fecha o **Recordset** ou o *Destination*, de forma que é possível continuar a trabalhar com o **Recordset** e salvar as alterações mais recentes. *Destination* permanece aberto até que o **Recordset** seja fechado.</span><span class="sxs-lookup"><span data-stu-id="881dc-p107">**Save** does not close the **Recordset** or *Destination*, so you can continue to work with the **Recordset** and save your most recent changes. *Destination* remains open until the **Recordset** is closed.</span></span>

<span data-ttu-id="881dc-p108">Por motivos de segurança, o método **Save** permite apenas a utilização de definições de segurança baixas e personalizadas a partir de um script executado pelo Microsoft Internet Explorer. Para obter uma explicação mais detalhada dos problemas de segurança, consulte "ADO and RDS Security Issues in Microsoft Internet Explorer" sob Artigos Técnicos do ActiveX Data Objects (ADO) nos Artigos Técnicos de Acesso a Dados da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="881dc-p108">For reasons of security, the **Save** method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer. For a more detailed explanation of security issues, see "ADO and RDS Security Issues in Microsoft Internet Explorer" under ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles.</span></span>

<span data-ttu-id="881dc-130">Se o método **Save** for chamado enquanto uma operação de busca, execução ou atualização assíncrona de **Recordset** estiver em andamento, **Save** aguardará até que a operação assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="881dc-130">If the **Save** method is called while an asynchronous **Recordset** fetch, execute, or update operation is in progress, then **Save** waits until the asynchronous operation is complete.</span></span>

<span data-ttu-id="881dc-p109">Os registros são salvos a partir da primeira linha do **Recordset**. Quando o método **Save** for concluído, a posição de linha atual será movida para a primeira linha do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="881dc-p109">Records are saved beginning with the first row of the **Recordset**. When the **Save** method is finished, the current row position is moved to the first row of the **Recordset**.</span></span>

<span data-ttu-id="881dc-p110">Para obter melhores resultados, defina a propriedade [CursorLocation](cursorlocation-property-ado.md) para **adUseClient** com **Save**. Se o provedor não oferecer suporte a toda a funcionalidade necessária para salvar objetos **Recordset**, o Cursor Service fornecerá essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="881dc-p110">For best results, set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient** with **Save**. If your provider does not support all of the functionality necessary to save **Recordset** objects, the Cursor Service will provide that functionality.</span></span>

<span data-ttu-id="881dc-p111">Quando um **Recordset** for persistido com a propriedade **CursorLocation** definida como **adUseServer**, a capacidade de atualização do **Recordset** será limitada. Normalmente, apenas atualizações, inserções e exclusões de tabela única são permitidas (dependendo da funcionalidade do provedor). O método [Resync](resync-method-ado.md) também está indisponível nessa configuração.</span><span class="sxs-lookup"><span data-stu-id="881dc-p111">When a **Recordset** is persisted with the **CursorLocation** property set to **adUseServer**, the update capability for the **Recordset** is limited. Typically, only single-table updates, insertions, and deletions are allowed (dependant upon provider functionality). The [Resync](resync-method-ado.md) method is also unavailable in this configuration.</span></span>


> [!NOTE]
> <P><span data-ttu-id="881dc-138">[!OBSERVAçãO] O salvamento de um <STRONG>Recordset</STRONG> com <STRONG>Fields</STRONG> do tipo <STRONG>adVariant</STRONG>, <STRONG>adIDispatch</STRONG> ou <STRONG>adIUnknown</STRONG> não é suportado pelo ADO e pode causar resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="881dc-138">Saving a <STRONG>Recordset</STRONG> with <STRONG>Fields</STRONG> of type <STRONG>adVariant</STRONG>, <STRONG>adIDispatch</STRONG>, or <STRONG>adIUnknown</STRONG> is not supported by ADO and can cause unpredictable results.</span></span></P>



<span data-ttu-id="881dc-139">Somente os **filtros** no formato de cadeias de caracteres de critérios (ex.: DataDoPedido \> ' 12/31/1999 ') afetam o conteúdo de um **Recordset**de persistido.</span><span class="sxs-lookup"><span data-stu-id="881dc-139">Only **Filters** in the form of Criteria Strings (e.g. OrderDate \> '12/31/1999') affect the contents of a persisted **Recordset**.</span></span> <span data-ttu-id="881dc-140">Os filtros criados com uma Matriz de **Bookmarks** ou utilizado um valor de **FilterGroupEnum** não afetarão o conteúdo do **Recordset** persistido.</span><span class="sxs-lookup"><span data-stu-id="881dc-140">Filters created with an Array of **Bookmarks** or using a value from the **FilterGroupEnum** will not affect the contents of the persisted **Recordset**.</span></span> <span data-ttu-id="881dc-141">Essas regras são aplicadas a **Recordsets** criados com cursores do cliente ou do servidor.</span><span class="sxs-lookup"><span data-stu-id="881dc-141">These rules apply to **Recordsets** created with either client-side or server-side cursors.</span></span>

<span data-ttu-id="881dc-142">Porque o parâmetro *Destination* pode aceitar qualquer objeto que dá suporte à interface IStream do OLE DB, é possível salvar um **Recordset** diretamente no objeto Response ASP.</span><span class="sxs-lookup"><span data-stu-id="881dc-142">Because the *Destination* parameter can accept any object that supports the OLE DB IStream interface, you can save a **Recordset** directly to the ASP Response object.</span></span> <span data-ttu-id="881dc-143">Para obter mais detalhes, consulte o [Cenário de Persistência de Recordset XML](xml-recordset-persistence-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="881dc-143">For more details, please see the [XML Recordset Persistence Scenario](xml-recordset-persistence-scenario.md).</span></span>

<span data-ttu-id="881dc-144">Também e possível salvar um **Recordset** em formato XML para uma instância de um objeto MSXML DOM, conforme mostrado no seguinte código Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="881dc-144">You can also save a **Recordset** in XML format to an instance of an MSXML DOM object, as is shown in the following Visual Basic code:</span></span>


> [!NOTE]
> <P><span data-ttu-id="881dc-p114">[!OBSERVAçãO] Duas limitações são aplicadas ao salvar <STRONG>Recordsets</STRONG> hierárquicos (formas de dados) em formato XML. Não é possível salvar em XML se o <STRONG>Recordset</STRONG> hierárquico contiver atualizações pendentes e não é possível salvar um <STRONG>Recordset</STRONG> hierárquico parametrizado.</span><span class="sxs-lookup"><span data-stu-id="881dc-p114">Two limitations apply when saving hierarchical <STRONG>Recordsets</STRONG> (data shapes) in XML format. You cannot save into XML if the hierarchical <STRONG>Recordset</STRONG> contains pending updates, and you cannot save a parameterized hierarchical <STRONG>Recordset</STRONG>.</span></span></P>



<span data-ttu-id="881dc-p115">Um Recordset salvo em formato XML é salvo utilizando-se o formato UTF-8. Quando um arquivo desse tipo for carregado em um Stream do ADO, o objeto Stream não tentará abrir um Recordset a partir do fluxo a menos que a propriedade Charset do fluxo esteja definida para o valor apropriado do formato UTF-8.</span><span class="sxs-lookup"><span data-stu-id="881dc-p115">A Recordset saved in XML format is saved using UTF-8 format. When such a file is loaded into an ADO Stream, the Stream object will not attempt to open a Recordset from the stream unless the Charset property of the stream is set to the appropriate value for UTF-8 format.</span></span>

