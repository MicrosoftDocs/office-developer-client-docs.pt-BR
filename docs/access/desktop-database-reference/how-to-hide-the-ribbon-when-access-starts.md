---
title: Ocultar a faixa de opções quando o Access for iniciado
TOCTitle: Hide the ribbon when Access starts
description: Este tópico descreve como carregar uma faixa de opções personalizada que oculta todas as guias internas no Access 2013.
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 384a575ae5e15b75ba7b0b891529c695cc3de599
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537826"
---
# <a name="hide-the-ribbon-when-access-starts"></a><span data-ttu-id="a9fd2-103">Ocultar a faixa de opções quando o Access for iniciado</span><span class="sxs-lookup"><span data-stu-id="a9fd2-103">Hide the ribbon when Access starts</span></span>

<span data-ttu-id="a9fd2-104">**Aplica-se ao:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9fd2-104">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="a9fd2-p101">Por padrão, o Microsoft Access não oferece um método para ocultar a faixa de opções. Este tópico descreve como carregar uma faixa de opções personalizada que oculta todas as guias internas.</span><span class="sxs-lookup"><span data-stu-id="a9fd2-p101">By default, Microsoft Access does not provide a method for hiding the ribbon. This topic describes how to load a customized ribbon that hides all of the built-in tabs.</span></span>

<span data-ttu-id="a9fd2-107">Para carregar a faixa de opções personalizada quando o Access for iniciado, você deverá armazenar suas configurações em uma tabela chamada **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="a9fd2-107">To load the customized ribbon when Access starts, you should store its settings in a table named **USysRibbons**.</span></span>

<span data-ttu-id="a9fd2-108">A tabela **USysRibbons** deve ser criada usando nomes de coluna específicos para que as personalizações da faixa de opções sejam implementadas.</span><span class="sxs-lookup"><span data-stu-id="a9fd2-108">The **USysRibbons** table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="a9fd2-109">A tabela a seguir lista as configurações para usar ao criar a tabela **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="a9fd2-109">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9fd2-110">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="a9fd2-110">Column name</span></span></p></th>
<th><p><span data-ttu-id="a9fd2-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a9fd2-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="a9fd2-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9fd2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9fd2-113"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="a9fd2-113"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="a9fd2-114">Texto</span><span class="sxs-lookup"><span data-stu-id="a9fd2-114">Text</span></span></p></td>
<td><p><span data-ttu-id="a9fd2-115">Contém o nome da faixa de opções personalizada a ser associado à esta personalização.</span><span class="sxs-lookup"><span data-stu-id="a9fd2-115">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9fd2-116"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="a9fd2-116"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="a9fd2-117">Memorando</span><span class="sxs-lookup"><span data-stu-id="a9fd2-117">Memo</span></span></p></td>
<td><p><span data-ttu-id="a9fd2-118">Contém o XML de extensibilidade da Faixa de Opções (RibbonX) que define a personalização da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="a9fd2-118">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="a9fd2-119">A tabela a seguir lista as configurações de personalização da faixa de opções a ser armazenada na tabela **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="a9fd2-119">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

|<span data-ttu-id="a9fd2-120">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="a9fd2-120">Column name</span></span>|<span data-ttu-id="a9fd2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a9fd2-121">Value</span></span>|
|:----------|:----|
|<span data-ttu-id="a9fd2-122">**RibbonName**</span><span class="sxs-lookup"><span data-stu-id="a9fd2-122">**RibbonName**</span></span>|<span data-ttu-id="a9fd2-123">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="a9fd2-123">HideTheRibbon</span></span>|
|<span data-ttu-id="a9fd2-124">**RibbonXML**</span><span class="sxs-lookup"><span data-stu-id="a9fd2-124">**RibbonXML**</span></span>|`<CustomUI xmlns="http://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="a9fd2-125">Aplicar uma faixa de opções personalizada quando o Access iniciar</span><span class="sxs-lookup"><span data-stu-id="a9fd2-125">Apply a custom ribbon when Access starts</span></span>

<span data-ttu-id="a9fd2-126">Para aplicar uma faixa de opções personalizada de forma que ela esteja disponível quando o aplicativo for iniciado, use o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="a9fd2-126">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="a9fd2-127">Siga o processo descrito anteriormente para disponibilizar a faixa de opções personalizada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a9fd2-127">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="a9fd2-128">Feche e então reinicie o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a9fd2-128">Close and then restart the application.</span></span>

3.  <span data-ttu-id="a9fd2-129">Escolha o **Botão Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), e escolha **Opções de Acesso**.</span><span class="sxs-lookup"><span data-stu-id="a9fd2-129">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="a9fd2-130">Escolha a opção **Banco de Dados Atual** e, em seguida, na seção **Opções da Faixa de Opções e da Barra de Ferramentas**, escolha a lista **Nome da Faixa de Opções** e selecione **HideTheRibbon**.</span><span class="sxs-lookup"><span data-stu-id="a9fd2-130">Choose the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, choose the **Ribbon Name** list and select **HideTheRibbon**.</span></span>

5.  <span data-ttu-id="a9fd2-131">Feche e então reinicie o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a9fd2-131">Close and then restart the application.</span></span>

> [!NOTE]
> <span data-ttu-id="a9fd2-132">Para saber mais sobre a interface do usuário da faixa de opções em outros aplicativos do Office, consulte [Visão geral da faixa de opções do Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="a9fd2-132">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


