---
title: Ocultar a faixa de opções ao iniciar o Access
TOCTitle: Hide the ribbon when Access starts
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b2b3e28157662a585fa03353da92a598b96bd2c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462632"
---
# <a name="hide-the-ribbon-when-access-starts"></a><span data-ttu-id="2a2ac-102">Ocultar a faixa de opções ao iniciar o Access</span><span class="sxs-lookup"><span data-stu-id="2a2ac-102">Hide the ribbon when Access starts</span></span>

<span data-ttu-id="2a2ac-103">**Aplica-se a:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a2ac-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="2a2ac-p101">Por padrão, o Microsoft Access não oferece um método para ocultar a faixa de opções. Este tópico descreve como carregar uma faixa de opções personalizada que oculta todas as guias internas.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-p101">By default, Microsoft Access does not provide a method for hiding the ribbon. This topic describes how to load a customized ribbon that hides all of the built-in tabs.</span></span>

<span data-ttu-id="2a2ac-106">Para carregar a faixa de opções personalizada quando o Access for iniciado, você deverá armazenar suas configurações em uma tabela chamada **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-106">To load the customized ribbon when Access starts, you should store its settings in a table named **USysRibbons**.</span></span>

<span data-ttu-id="2a2ac-p102">A tabela **USysRibbons** deve ser criada usando nomes de coluna específicos para que as personalizações da faixa de opções a serem implementadas. A tabela a seguir lista as configurações a serem usadas na criação da tabela **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-p102">The **USysRibbons** table must be created using specific column names in order for the ribbon customizations to be implemented. The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2a2ac-109">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="2a2ac-109">Column Name</span></span></p></th>
<th><p><span data-ttu-id="2a2ac-110">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2a2ac-110">Data Type</span></span></p></th>
<th><p><span data-ttu-id="2a2ac-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a2ac-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a2ac-112"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="2a2ac-112"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="2a2ac-113">Texto</span><span class="sxs-lookup"><span data-stu-id="2a2ac-113">Text</span></span></p></td>
<td><p><span data-ttu-id="2a2ac-114">Contém o nome da faixa de opções personalizada a ser associado à esta personalização.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-114">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a2ac-115"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="2a2ac-115"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="2a2ac-116">Memorando</span><span class="sxs-lookup"><span data-stu-id="2a2ac-116">Memo</span></span></p></td>
<td><p><span data-ttu-id="2a2ac-117">Contém o XML de Extensibilidade da Faixa de Opções (RibbonX) que define a personalização da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-117">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2a2ac-118">A tabela a seguir lista as configurações de personalização da faixa de opções a serem armazenadas na tabela **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-118">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2a2ac-119">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="2a2ac-119">Column Name</span></span></p></th>
<th><p><span data-ttu-id="2a2ac-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2a2ac-120">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a2ac-121"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="2a2ac-121"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="2a2ac-122">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="2a2ac-122">HideTheRibbon</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a2ac-123"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="2a2ac-123"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="2a2ac-124">&lt;CustomUI xmlns =&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot; &gt; &lt;startFromScratch da faixa de opções =&quot;true&quot;/&gt;&lt;/CustomUI&gt;</span><span class="sxs-lookup"><span data-stu-id="2a2ac-124">&lt;CustomUI xmlns=&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot;&gt; &lt;ribbon startFromScratch=&quot;true&quot;/&gt;&lt;/CustomUI&gt;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="applying-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="2a2ac-125">Aplicando uma faixa de opções personalizada quando o Access é iniciado</span><span class="sxs-lookup"><span data-stu-id="2a2ac-125">Applying a Custom Ribbon When Access Starts</span></span>

<span data-ttu-id="2a2ac-126">Para aplicar uma faixa de opções personalizada de forma que ela esteja disponível quando o aplicativo for iniciado, use o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="2a2ac-126">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="2a2ac-127">Siga o processo descrito anteriormente para disponibilizar a faixa de opções personalizada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-127">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="2a2ac-128">Feche e então reinicie o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-128">Close and then restart the application.</span></span>

3.  <span data-ttu-id="2a2ac-129">Clique no **Botão do Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") e clique em **Opções do Access**.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-129">Click the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then click **Access Options**.</span></span>

4.  <span data-ttu-id="2a2ac-130">Clique na opção **Banco de Dados Atual** e, em seguida, na seção **Opções da Faixa de Opções e da Barra de Ferramentas**, clique na lista **Nome da Faixa de Opções** e selecione **HideTheRibbon**.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-130">Click the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select **HideTheRibbon**.</span></span>

5.  <span data-ttu-id="2a2ac-131">Feche e então reinicie o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-131">Close and then restart the application.</span></span>

> [!NOTE]
> <span data-ttu-id="2a2ac-132">[!OBSERVAçãO] Para saber mais sobre a interface do usuário da faixa de opções em outros aplicativos do Office, consulte [Visão geral da faixa de opções do Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="2a2ac-132">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


