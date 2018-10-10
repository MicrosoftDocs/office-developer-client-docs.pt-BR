---
title: 'HelloData: um aplicativo ADO simples'
TOCTitle: 'HelloData: A Simple ADO Application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f7a3ef1f8b1a183bcef760af28d6eb8a849b17aa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462251"
---
# <a name="hellodata-a-simple-ado-application"></a><span data-ttu-id="352f0-102">HelloData: um aplicativo ADO simples</span><span class="sxs-lookup"><span data-stu-id="352f0-102">HelloData: A Simple ADO Application</span></span>


<span data-ttu-id="352f0-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="352f0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="352f0-p101">Para preparar a infraestrutura para uma exploração da biblioteca do ADO, considere um aplicativo ADO simples, denominado "HelloData." Esse aplicativo consulta por etapas cada uma das quatro operações principais do ADO (obtenção, exame, edição e atualização de dados). Para enfocar os conceitos básicos do ADO e impedir a desordem de códigos será feito um tratamento mínimo de erros no exemplo.</span><span class="sxs-lookup"><span data-stu-id="352f0-p101">To lay the groundwork for an exploration of the ADO library, consider a simple ADO application called "HelloData." HelloData steps through each of the four major ADO operations (getting, examining, editing, and updating data). In order to focus on the fundamentals of ADO and prevent code clutter, minimal error handling is done in the example.</span></span>

<span data-ttu-id="352f0-107">O aplicativo consulta o banco de dados de exemplo Northwind, incluído no Microsoft SQL Server 2000.</span><span class="sxs-lookup"><span data-stu-id="352f0-107">The application queries the Northwind sample database that is included with Microsoft SQL Server 2000.</span></span>

<span data-ttu-id="352f0-108">**Para executar o HelloData**</span><span class="sxs-lookup"><span data-stu-id="352f0-108">**To run HelloData**</span></span>

1.  <span data-ttu-id="352f0-109">Crie um novo Projeto Executável Padrão do Visual Basic que faça referências à biblioteca do ADO 2.5.</span><span class="sxs-lookup"><span data-stu-id="352f0-109">Create a new Standard Executable Visual Basic Project that references the ADO 2.5 library.</span></span>

2.  <span data-ttu-id="352f0-110">Crie quatro botões de comando na parte superior do formulário, definindo as propriedades **Name** e **Caption** como os valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="352f0-110">Create four command buttons at the top of the form, setting the **Name** and **Caption** properties to the values shown in the table below.</span></span>

3.  <span data-ttu-id="352f0-111">Abaixo dos botões, adicione um **Controle de DataGrid da Microsoft** (Msdatgrd.ocx).</span><span class="sxs-lookup"><span data-stu-id="352f0-111">Below the buttons, add a **Microsoft DataGrid Control** (Msdatgrd.ocx).</span></span> <span data-ttu-id="352f0-112">O arquivo Msdatgrd.ocx vem com o Visual Basic e está localizado em sua \\windows\\system32 ou \\winnt\\diretório system32.</span><span class="sxs-lookup"><span data-stu-id="352f0-112">The Msdatgrd.ocx file comes with Visual Basic and is located in your \\windows\\system32 or \\winnt\\system32 directory.</span></span> <span data-ttu-id="352f0-113">Para adicionar o controle DataGrid ao painel de ferramentas do Visual Basic, selecione **componentes …** no menu **projeto** .</span><span class="sxs-lookup"><span data-stu-id="352f0-113">To add the DataGrid control to your Visual Basic toolbox pane, select **Components...** from the **Project** menu.</span></span> <span data-ttu-id="352f0-114">Em seguida, marque a caixa ao lado de "Microsoft controle DataGrid 6.0 (SP3) (OLEDB)" e clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="352f0-114">Then check the box next to "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" and click **OK**.</span></span> <span data-ttu-id="352f0-115">Para adicionar o controle ao projeto, arraste o controle DataGrid da caixa de ferramentas para o formulário do Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="352f0-115">To add the control to the project, drag the DataGrid control from the Toolbox to the Visual Basic form.</span></span>

4.  <span data-ttu-id="352f0-p103">Crie uma **TextBox** no formulário abaixo da grade e defina as propriedades como mostra a tabela. O formulário deverá ter uma aparência semelhante à figura a seguir, quando você tiver finalizado.</span><span class="sxs-lookup"><span data-stu-id="352f0-p103">Create a **TextBox** on the form below the grid and set its properties as shown in the table. The form should look similar to the following figure when you are finished.</span></span>

5.  <span data-ttu-id="352f0-p104">Finalmente, copie o código listado em "[Código do HelloData](hellodata-code.md)" e cole-o na janela do editor de códigos do formulário. Pressione **F5** para executar o código.</span><span class="sxs-lookup"><span data-stu-id="352f0-p104">Finally, copy the code listed in "[HelloData Code](hellodata-code.md)" and paste it into the code editor window of the form. Press **F5** to run the code.</span></span>


> [!NOTE]
> <P><span data-ttu-id="352f0-p105">[!OBSERVAçãO] No exemplo a seguir e por todo o guia, o id de usuário "MyId" com a senha "123aBc" será usado para se autenticar no servidor. Você deve substituir esses valores com as credenciais de logon válidas do servidor. Além disso, substitua o valor "MyServer" pelo nome do seu servidor.</span><span class="sxs-lookup"><span data-stu-id="352f0-p105">In the following example, and throughout the guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server. You should substitute these values with valid logon credentials for your server. Also, substitute the "MyServer" value with the name of your server.</span></span></P>



<span data-ttu-id="352f0-123">Para obter uma descrição detalhada do código, consulte "[Detalhes do HelloData](hellodata-details.md)."</span><span class="sxs-lookup"><span data-stu-id="352f0-123">For a detailed description of the code, see "[HelloData Details](hellodata-details.md)."</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="352f0-124">Tipo de controle</span><span class="sxs-lookup"><span data-stu-id="352f0-124">Control Type</span></span></p></th>
<th><p><span data-ttu-id="352f0-125">Propriedade</span><span class="sxs-lookup"><span data-stu-id="352f0-125">Property</span></span></p></th>
<th><p><span data-ttu-id="352f0-126">Valor</span><span class="sxs-lookup"><span data-stu-id="352f0-126">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="352f0-127">Formulário</span><span class="sxs-lookup"><span data-stu-id="352f0-127">Form</span></span></p></td>
<td><p><span data-ttu-id="352f0-128">Name</span><span class="sxs-lookup"><span data-stu-id="352f0-128">Name</span></span></p></td>
<td><p><span data-ttu-id="352f0-129">Form1</span><span class="sxs-lookup"><span data-stu-id="352f0-129">Form1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="352f0-130">Height</span><span class="sxs-lookup"><span data-stu-id="352f0-130">Height</span></span></p></td>
<td><p><span data-ttu-id="352f0-131">6500</span><span class="sxs-lookup"><span data-stu-id="352f0-131">6500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="352f0-132">Width</span><span class="sxs-lookup"><span data-stu-id="352f0-132">Width</span></span></p></td>
<td><p><span data-ttu-id="352f0-133">6500</span><span class="sxs-lookup"><span data-stu-id="352f0-133">6500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352f0-134">MS DataGrid</span><span class="sxs-lookup"><span data-stu-id="352f0-134">MS DataGrid</span></span></p></td>
<td><p><span data-ttu-id="352f0-135">Name</span><span class="sxs-lookup"><span data-stu-id="352f0-135">Name</span></span></p></td>
<td><p><span data-ttu-id="352f0-136">grdDisplay1</span><span class="sxs-lookup"><span data-stu-id="352f0-136">grdDisplay1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352f0-137">Caixa de texto</span><span class="sxs-lookup"><span data-stu-id="352f0-137">TextBox</span></span></p></td>
<td><p><span data-ttu-id="352f0-138">Name</span><span class="sxs-lookup"><span data-stu-id="352f0-138">Name</span></span></p></td>
<td><p><span data-ttu-id="352f0-139">txtDisplay1</span><span class="sxs-lookup"><span data-stu-id="352f0-139">txtDisplay1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="352f0-140">Multiline</span><span class="sxs-lookup"><span data-stu-id="352f0-140">Multiline</span></span></p></td>
<td><p><span data-ttu-id="352f0-141">true</span><span class="sxs-lookup"><span data-stu-id="352f0-141">true</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352f0-142">Botão de Comando</span><span class="sxs-lookup"><span data-stu-id="352f0-142">Command Button</span></span></p></td>
<td><p><span data-ttu-id="352f0-143">Name</span><span class="sxs-lookup"><span data-stu-id="352f0-143">Name</span></span></p></td>
<td><p><span data-ttu-id="352f0-144">cmdGetData</span><span class="sxs-lookup"><span data-stu-id="352f0-144">cmdGetData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="352f0-145">Caption</span><span class="sxs-lookup"><span data-stu-id="352f0-145">Caption</span></span></p></td>
<td><p><span data-ttu-id="352f0-146">Get Data</span><span class="sxs-lookup"><span data-stu-id="352f0-146">Get Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352f0-147">Botão de Comando</span><span class="sxs-lookup"><span data-stu-id="352f0-147">Command Button</span></span></p></td>
<td><p><span data-ttu-id="352f0-148">Name</span><span class="sxs-lookup"><span data-stu-id="352f0-148">Name</span></span></p></td>
<td><p><span data-ttu-id="352f0-149">cmdExamineData</span><span class="sxs-lookup"><span data-stu-id="352f0-149">cmdExamineData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="352f0-150">Caption</span><span class="sxs-lookup"><span data-stu-id="352f0-150">Caption</span></span></p></td>
<td><p><span data-ttu-id="352f0-151">Examine Data</span><span class="sxs-lookup"><span data-stu-id="352f0-151">Examine Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352f0-152">Botão de Comando</span><span class="sxs-lookup"><span data-stu-id="352f0-152">Command Button</span></span></p></td>
<td><p><span data-ttu-id="352f0-153">Name</span><span class="sxs-lookup"><span data-stu-id="352f0-153">Name</span></span></p></td>
<td><p><span data-ttu-id="352f0-154">cmdEditData</span><span class="sxs-lookup"><span data-stu-id="352f0-154">cmdEditData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="352f0-155">Caption</span><span class="sxs-lookup"><span data-stu-id="352f0-155">Caption</span></span></p></td>
<td><p><span data-ttu-id="352f0-156">Edit Data</span><span class="sxs-lookup"><span data-stu-id="352f0-156">Edit Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352f0-157">Botão de Comando</span><span class="sxs-lookup"><span data-stu-id="352f0-157">Command Button</span></span></p></td>
<td><p><span data-ttu-id="352f0-158">Name</span><span class="sxs-lookup"><span data-stu-id="352f0-158">Name</span></span></p></td>
<td><p><span data-ttu-id="352f0-159">cmdUpdateData</span><span class="sxs-lookup"><span data-stu-id="352f0-159">cmdUpdateData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="352f0-160">Caption</span><span class="sxs-lookup"><span data-stu-id="352f0-160">Caption</span></span></p></td>
<td><p><span data-ttu-id="352f0-161">Update Data</span><span class="sxs-lookup"><span data-stu-id="352f0-161">Update Data</span></span></p></td>
</tr>
</tbody>
</table>

