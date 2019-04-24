---
title: Ação da macro ImportarListadoSharePoint
TOCTitle: ImportSharePointList macro action
ms:assetid: 6a633d7d-d81d-0e2e-6c1c-706a552c1bf2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195403(v=office.15)
ms:contentKeyID: 48545429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152234
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: df77d2375b66df907832b6ff2717427ae54a35a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291856"
---
# <a name="importsharepointlist-macro-action"></a><span data-ttu-id="10773-102">Ação da macro ImportarListadoSharePoint</span><span class="sxs-lookup"><span data-stu-id="10773-102">ImportSharePointList macro action</span></span>

<span data-ttu-id="10773-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="10773-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="10773-104">É possível usar a ação **ImportarListadoSharePoint** para importar ou vincular dados de um site do Microsoft SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="10773-104">You can use the **ImportSharePointList** action to import or link data from a Microsoft SharePoint Foundation site.</span></span>

> [!NOTE]
> <span data-ttu-id="10773-105">[!OBSERVAçãO] This action will not be allowed if the database is not trusted.</span><span class="sxs-lookup"><span data-stu-id="10773-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="10773-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="10773-106">Setting</span></span>

<span data-ttu-id="10773-107">A ação **ImportarListadoSharePoint** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="10773-107">The **ImportSharePointList** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10773-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="10773-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="10773-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="10773-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10773-110"><strong>Tipo de transferência</strong></span><span class="sxs-lookup"><span data-stu-id="10773-110"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="10773-111">Selecione o tipo de transferência.</span><span class="sxs-lookup"><span data-stu-id="10773-111">Select the type of transfer.</span></span></p>
<ul>
<li><p><span data-ttu-id="10773-112">Selecione <strong>importar</strong> para copiar os dados do SharePoint Foundation em uma tabela no Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="10773-112">Select <strong>Import</strong> to copy the SharePoint Foundation data into a table in Microsoft Access.</span></span> <span data-ttu-id="10773-113">As atualizações dos dados no Access não afetam os dados no SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="10773-113">Updates to the data in Access do not affect the data in SharePoint Foundation.</span></span> <span data-ttu-id="10773-114">Da mesma forma, as atualizações dos dados no SharePoint Foundation não afetam os dados no Access.</span><span class="sxs-lookup"><span data-stu-id="10773-114">Likewise, updates to the data in SharePoint Foundation do not affect the data in Access.</span></span></p></li>
<li><p><span data-ttu-id="10773-115">Selecione <strong>vincular</strong> para criar uma tabela vinculada no Access que vincule aos dados no SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="10773-115">Select <strong>Link</strong> to create a linked table in Access that links to the data in SharePoint Foundation.</span></span> <span data-ttu-id="10773-116">As atualizações dos dados no Access são refletidas no SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="10773-116">Updates to the data in Access are reflected in SharePoint Foundation.</span></span> <span data-ttu-id="10773-117">Da mesma forma, as atualizações dos dados no SharePoint Foundation são refletidas no Access.</span><span class="sxs-lookup"><span data-stu-id="10773-117">Likewise, updates to the data in SharePoint Foundation are reflected in Access.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10773-118"><strong>Endereço do site</strong></span><span class="sxs-lookup"><span data-stu-id="10773-118"><strong>Site Address</strong></span></span></p></td>
<td><p><span data-ttu-id="10773-119">Digite o caminho completo do site do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="10773-119">Enter the full path of the SharePoint site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10773-120"><strong>ID da lista</strong></span><span class="sxs-lookup"><span data-stu-id="10773-120"><strong>List ID</strong></span></span></p></td>
<td><p><span data-ttu-id="10773-121">Digite o nome ou o GUID da lista a ser transferida.</span><span class="sxs-lookup"><span data-stu-id="10773-121">Enter the name or GUID of the list to be transferred.</span></span> <span data-ttu-id="10773-122">Argumento necessário.</span><span class="sxs-lookup"><span data-stu-id="10773-122">Required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10773-123"><strong>ID do modo de exibição</strong></span><span class="sxs-lookup"><span data-stu-id="10773-123"><strong>View ID</strong></span></span></p></td>
<td><p><span data-ttu-id="10773-p104">Digite o GUID do modo de exibição para a lista que deseja usar. Deixe este argumento em branco para transferir todas as linhas e colunas da lista.</span><span class="sxs-lookup"><span data-stu-id="10773-p104">Enter the GUID of the view for the list you want to use. Leave this argument blank to transfer all rows and columns in the list.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10773-126"><strong>Nome da Tabela</strong></span><span class="sxs-lookup"><span data-stu-id="10773-126"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="10773-127">Digite o nome a ser exibido da tabela ou da tabela vinculada no Access.</span><span class="sxs-lookup"><span data-stu-id="10773-127">Enter the name you want displayed for the table or linked table in Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10773-128"><strong>Obter valores de exibição da pesquisa</strong></span><span class="sxs-lookup"><span data-stu-id="10773-128"><strong>Get Lookup Display Values</strong></span></span></p></td>
<td><p><span data-ttu-id="10773-129">Selecione <strong>Sim</strong> para transferir valores de exibição para os campos Pesquisa, em vez da ID usada para executar a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="10773-129">Select <strong>Yes</strong> to transfer display values for Lookup fields instead of the ID used to perform the lookup.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="10773-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="10773-130">Remarks</span></span>

- <span data-ttu-id="10773-131">Esta ação tem o mesmo efeito de clicar em **Lista do SharePoint** no grupo **Importar** da guia **Dados Externos**. Os argumentos da ação correspondem às escolhas feitas no Assistente para Obter Dados Externos.</span><span class="sxs-lookup"><span data-stu-id="10773-131">This action has the same effect as clicking **SharePoint List** in the **Import** group on the **External Data** tab. The arguments for the action correspond to the choices you make in the Get External Data Wizard.</span></span>

- <span data-ttu-id="10773-132">Para executar a ação **ImportarListadoSharePoint** em um módulo do VBA, use o método **TrasnferirListadoSharePoint** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="10773-132">To run the **ImportSharePointList** action in a VBA module, use the **TransferSharePointList** method of the **DoCmd** object.</span></span>

- <span data-ttu-id="10773-133">Se você especificar uma lista ou um modo de exibição inexistente, nenhum erro ocorrerá e nenhum dado será transferido.</span><span class="sxs-lookup"><span data-stu-id="10773-133">If you specify a nonexistent list or view, no error occurs, and no data is transferred.</span></span>

- <span data-ttu-id="10773-p105">Um GUID é um identificador hexadecimal exclusivo de uma lista ou de um modo de exibição. Um GUID deve ser inserido no formato a seguir, em que cada "F" é um número hexadecimal (0 a 9 ou A a F).</span><span class="sxs-lookup"><span data-stu-id="10773-p105">A GUID is a unique hexadecimal identifier for a list or a view. A GUID must be entered in the following format, where each "F" is a hexadecimal number (0 through 9 or A through F).</span></span>
    
  `{FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF}`
    
  <span data-ttu-id="10773-136">Você pode obter o GUID de uma lista ou de um modo de exibição no site do SharePoint usando o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="10773-136">You can obtain the GUID for a list or view from the SharePoint site by using the following procedure:</span></span>
    
  1. <span data-ttu-id="10773-137">Abra a lista no SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="10773-137">Open the list in SharePoint Foundation.</span></span>
    
  2. <span data-ttu-id="10773-138">Se o modo de exibição desejado não for exibido, clique na seta suspensa **Modo de Exibição** e selecione o modo de exibição desejado.</span><span class="sxs-lookup"><span data-stu-id="10773-138">If the view you want is not displayed, click the **View** drop-down arrow and then select the view you want.</span></span>
    
  3. <span data-ttu-id="10773-139">Clique na seta suspensa **Modo de Exibição** e selecione **Modificar este Modo de Exibição**.O endereço na barra de endereços do navegador contém os GUIDs da lista e do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="10773-139">Click the **View** drop-down arrow and then select **Modify this View**.The address in the browser's address bar contains the GUIDs for both the list and the view.</span></span> <span data-ttu-id="10773-140">O GUID da lista vem depois de **List=** e o do modo de exibição, depois de **View=**.</span><span class="sxs-lookup"><span data-stu-id="10773-140">The GUID for the list follows **List=**, and the GUID for the view follows **View=**.</span></span> <span data-ttu-id="10773-141">No entanto, no endereço, cada caractere **{** (chave esquerda) é representado pela cadeia de caracteres **%7B**, cada caractere **-** (hífen) é representado pela cadeia de caracteres **%2D** e cada caractere **}** (chave direita) é representado pela cadeia de caracteres **%7D**.</span><span class="sxs-lookup"><span data-stu-id="10773-141">However, in the address, each **{** (left brace) character is represented by the string **%7B**, each **-** (hyphen) character is represented by the string **%2D**, and each **}** (right brace) character is represented by the string **%7D**.</span></span> <span data-ttu-id="10773-142">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="10773-142">For example:</span></span>
        
     `https://MySite12/_layouts/ViewEdit.aspx?List=%7B2A82A404%2D5529%2D47DC%2DAE13%2DAC1D9BC0A84F%7D&View=%7B357B4FE6%2D44CF%2D4275%2DB91F%2D46558301579B%7D`
        
  <span data-ttu-id="10773-143">Antes de poder usar os GUIDs do endereço como argumentos nesta ação de macro, você deve substituir cada cadeia de caracteres **% 7B** pelo caractere **{** , substituir cada cadeia de caracteres **% 2D** pelo **-** caractere e substituir cada cadeia de caracteres **% 7D** por **}** caractere.</span><span class="sxs-lookup"><span data-stu-id="10773-143">Before you can use the GUIDs from the address as arguments in this macro action, you must replace each **%7B** string with the **{** character, replace each **%2D** string with the **-** character, and replace each **%7D** string with the **}** character.</span></span> <span data-ttu-id="10773-144">Não inclua o caractere **&** (E comercial) que vem depois da cadeia de caracteres **%7D** no GUID da lista.</span><span class="sxs-lookup"><span data-stu-id="10773-144">Do not include the **&** (ampersand) character that follows the **%7D** string in the list GUID.</span></span>

