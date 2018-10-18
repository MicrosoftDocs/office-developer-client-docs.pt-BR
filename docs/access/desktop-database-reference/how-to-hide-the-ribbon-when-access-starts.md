---
<span data-ttu-id="70a60-101">título: ocultar a faixa de opções ao iniciar o Access TOCTitle: ocultar a faixa de opções ao iniciar o Access <<<<<<< ms:assetid cabeça: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: ms.date 48548817: 18/09/2015 === Descrição: como carregar uma faixa de opções personalizada que oculta todas as guias internas no Access 2013.</span><span class="sxs-lookup"><span data-stu-id="70a60-101">title: Hide the ribbon when Access starts TOCTitle: Hide the ribbon when Access starts <<<<<<< HEAD ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: 48548817 ms.date: 09/18/2015 ======= description: How to load a customized ribbon that hides all of the built-in tabs in Access 2013.</span></span>
<span data-ttu-id="70a60-102">MS:AssetID: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: ms.date 48548817: 10/16/2018</span><span class="sxs-lookup"><span data-stu-id="70a60-102">ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: 48548817 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="70a60-103">mtps_version mestre: v=office.15</span><span class="sxs-lookup"><span data-stu-id="70a60-103">master mtps_version: v=office.15</span></span>
---

# <a name="hide-the-ribbon-when-access-starts"></a><span data-ttu-id="70a60-104">Ocultar a faixa de opções ao iniciar o Access</span><span class="sxs-lookup"><span data-stu-id="70a60-104">Hide the ribbon when Access starts</span></span>

<span data-ttu-id="70a60-105">**Aplica-se a:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="70a60-105">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="70a60-p102">Por padrão, o Microsoft Access não oferece um método para ocultar a faixa de opções. Este tópico descreve como carregar uma faixa de opções personalizada que oculta todas as guias internas.</span><span class="sxs-lookup"><span data-stu-id="70a60-p102">By default, Microsoft Access does not provide a method for hiding the ribbon. This topic describes how to load a customized ribbon that hides all of the built-in tabs.</span></span>

<span data-ttu-id="70a60-108">Para carregar a faixa de opções personalizada quando o Access for iniciado, você deverá armazenar suas configurações em uma tabela chamada **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="70a60-108">To load the customized ribbon when Access starts, you should store its settings in a table named **USysRibbons**.</span></span>

<span data-ttu-id="70a60-109"><<<<<<< Cabeça tabela **USysRibbons** deve ser criada usando nomes de coluna específica na ordem para as personalizações de faixa de opções a serem implementadas.</span><span class="sxs-lookup"><span data-stu-id="70a60-109"><<<<<<< HEAD The **USysRibbons** table must be created using specific column names in order for the ribbon customizations to be implemented.</span></span> <span data-ttu-id="70a60-110">A tabela a seguir lista as configurações a serem usadas na criação da tabela **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="70a60-110">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
<span data-ttu-id="70a60-111">=== Tabela **USysRibbons** deve ser criada com o uso de nomes de coluna específica para as personalizações de faixa de opções a serem implementadas.</span><span class="sxs-lookup"><span data-stu-id="70a60-111">======= The **USysRibbons** table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="70a60-112">A tabela a seguir lista as configurações a serem usadas na criação da tabela **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="70a60-112">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
>>>>>>> <span data-ttu-id="70a60-113">mestre</span><span class="sxs-lookup"><span data-stu-id="70a60-113">master</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<span data-ttu-id="70a60-114"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="70a60-114"><<<<<<< HEAD</span></span>
<th><p><span data-ttu-id="70a60-115">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="70a60-115">Column Name</span></span></p></th>
<th><p><span data-ttu-id="70a60-116">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="70a60-116">Data Type</span></span></p></th>
=======
<th><p><span data-ttu-id="70a60-117">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="70a60-117">Column name</span></span></p></th>
<th><p><span data-ttu-id="70a60-118">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="70a60-118">Data type</span></span></p></th><span data-ttu-id="70a60-119">
>>>>>>>mestre</span><span class="sxs-lookup"><span data-stu-id="70a60-119">
>>>>>>> master</span></span>
<th><p><span data-ttu-id="70a60-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="70a60-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70a60-121"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="70a60-121"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="70a60-122">Texto</span><span class="sxs-lookup"><span data-stu-id="70a60-122">Text</span></span></p></td>
<td><p><span data-ttu-id="70a60-123">Contém o nome da faixa de opções personalizada a ser associado à esta personalização.</span><span class="sxs-lookup"><span data-stu-id="70a60-123">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70a60-124"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="70a60-124"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="70a60-125">Memorando</span><span class="sxs-lookup"><span data-stu-id="70a60-125">Memo</span></span></p></td>
<span data-ttu-id="70a60-126"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="70a60-126"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="70a60-127">Contém o XML de Extensibilidade da Faixa de Opções (RibbonX) que define a personalização da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="70a60-127">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
=======
<td><p><span data-ttu-id="70a60-128">Contém a extensibilidade da faixa de opções XML (RibbonX) que define a personalização da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="70a60-128">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td><span data-ttu-id="70a60-129">
>>>>>>>mestre</span><span class="sxs-lookup"><span data-stu-id="70a60-129">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>

<span data-ttu-id="70a60-130"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="70a60-130"><<<<<<< HEAD</span></span>

<span data-ttu-id="70a60-131">A tabela a seguir lista as configurações de personalização da faixa de opções a serem armazenadas na tabela **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="70a60-131">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="70a60-132">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="70a60-132">Column Name</span></span></p></th>
<th><p><span data-ttu-id="70a60-133">Valor</span><span class="sxs-lookup"><span data-stu-id="70a60-133">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70a60-134"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="70a60-134"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="70a60-135">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="70a60-135">HideTheRibbon</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70a60-136"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="70a60-136"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="70a60-137">&lt;CustomUI xmlns =&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot; &gt; &lt;startFromScratch da faixa de opções =&quot;true&quot;/&gt;&lt;/CustomUI&gt;</span><span class="sxs-lookup"><span data-stu-id="70a60-137">&lt;CustomUI xmlns=&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot;&gt; &lt;ribbon startFromScratch=&quot;true&quot;/&gt;&lt;/CustomUI&gt;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="applying-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="70a60-138">Aplicando uma faixa de opções personalizada quando o Access é iniciado</span><span class="sxs-lookup"><span data-stu-id="70a60-138">Applying a Custom Ribbon When Access Starts</span></span>
=======
<br/>

<span data-ttu-id="70a60-139">A tabela a seguir lista as configurações de personalização da faixa de opções a serem armazenadas na tabela **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="70a60-139">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

|<span data-ttu-id="70a60-140">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="70a60-140">Column name</span></span>|<span data-ttu-id="70a60-141">Valor</span><span class="sxs-lookup"><span data-stu-id="70a60-141">Value</span></span>|
|:----------|:----|
|<span data-ttu-id="70a60-142">**RibbonName**</span><span class="sxs-lookup"><span data-stu-id="70a60-142">**RibbonName**</span></span>|<span data-ttu-id="70a60-143">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="70a60-143">HideTheRibbon</span></span>|
|<span data-ttu-id="70a60-144">**RibbonXML**</span><span class="sxs-lookup"><span data-stu-id="70a60-144">**RibbonXML**</span></span>|`<CustomUI xmlns="https://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="70a60-145">Aplicar uma faixa de opções personalizada ao iniciar o Access</span><span class="sxs-lookup"><span data-stu-id="70a60-145">Apply a custom ribbon when Access starts</span></span>
>>>>>>> <span data-ttu-id="70a60-146">mestre</span><span class="sxs-lookup"><span data-stu-id="70a60-146">master</span></span>

<span data-ttu-id="70a60-147">Para aplicar uma faixa de opções personalizada de forma que ela esteja disponível quando o aplicativo for iniciado, use o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="70a60-147">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="70a60-148">Siga o processo descrito anteriormente para disponibilizar a faixa de opções personalizada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="70a60-148">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="70a60-149">Feche e então reinicie o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="70a60-149">Close and then restart the application.</span></span>

<span data-ttu-id="70a60-150"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="70a60-150"><<<<<<< HEAD</span></span>
3.  <span data-ttu-id="70a60-151">Clique no **Botão do Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") e clique em **Opções do Access**.</span><span class="sxs-lookup"><span data-stu-id="70a60-151">Click the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then click **Access Options**.</span></span>

4.  <span data-ttu-id="70a60-152">Clique na opção **Banco de Dados Atual** e, em seguida, na seção **Opções da Faixa de Opções e da Barra de Ferramentas**, clique na lista **Nome da Faixa de Opções** e selecione **HideTheRibbon**.</span><span class="sxs-lookup"><span data-stu-id="70a60-152">Click the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select **HideTheRibbon**.</span></span>
=======
3.  <span data-ttu-id="70a60-153">Escolha o **Botão do Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102")e escolha **Opções do Access**.</span><span class="sxs-lookup"><span data-stu-id="70a60-153">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="70a60-154">Escolha a opção de **Banco de dados atual** e em seguida, na seção **Opções de barra de ferramentas e faixa de opções** , escolha a lista **Nome da faixa de opções** e selecione **HideTheRibbon**.</span><span class="sxs-lookup"><span data-stu-id="70a60-154">Choose the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, choose the **Ribbon Name** list and select **HideTheRibbon**.</span></span>
>>>>>>> <span data-ttu-id="70a60-155">mestre</span><span class="sxs-lookup"><span data-stu-id="70a60-155">master</span></span>

5.  <span data-ttu-id="70a60-156">Feche e então reinicie o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="70a60-156">Close and then restart the application.</span></span>

> [!NOTE]
> <span data-ttu-id="70a60-157">[!OBSERVAçãO] Para saber mais sobre a interface do usuário da faixa de opções em outros aplicativos do Office, consulte [Visão geral da faixa de opções do Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="70a60-157">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


