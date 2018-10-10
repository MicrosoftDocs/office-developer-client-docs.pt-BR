---
title: Inicializando o driver de fonte de dados do Microsoft Exchange
TOCTitle: Initializing the Microsoft Exchange Data Source Driver
ms:assetid: cf87a746-f846-1a01-f4ec-20a25e335193
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834677(v=office.15)
ms:contentKeyID: 48547810
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032667
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f711e9814e32742c89c37ae3357111143ca18b6e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462056"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a><span data-ttu-id="f65e4-102">Inicializando o driver de fonte de dados do Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="f65e4-102">Initializing the Microsoft Exchange Data Source Driver</span></span>

<span data-ttu-id="f65e4-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f65e4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f65e4-p101">Quando você instala o driver de fonte de dados do Microsoft® Exchange, o programa de instalação grava um conjunto de valores padrão no Registro do Microsoft Windows®, nas subchaves Engines e ISAM Formats. Você não deve modificar essas configurações diretamente; use o programa de instalação de seu aplicativo para adicionar, remover ou alterar essas configurações. As seções a seguir descrevem a inicialização e as configurações do ISAM Format no driver de fonte de dados do Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="f65e4-p101">When you install the Microsoft® Exchange Data Source driver, the Setup program writes a set of default values to the Microsoft Windows® Registry in the Engines and ISAM Formats subkeys. You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings. The following sections describe initialization and ISAM Format settings for the Microsoft Exchange Data Source driver.</span></span>

## <a name="microsoft-exchange-data-source-initialization-settings"></a><span data-ttu-id="f65e4-107">Configurações de inicialização da fonte de dados do Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="f65e4-107">Microsoft Exchange Data Source Initialization Settings</span></span>

<span data-ttu-id="f65e4-108">O **mecanismo de conectividade do Access\\mecanismos\\Exchange** pasta inclui configurações de inicialização para o driver Aceexch.dll, usada para acesso externo às pastas do Microsoft Outlook e Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="f65e4-108">The **Access Connectivity Engine\\Engines\\Exchange** folder includes initialization settings for the Aceexch.dll driver, used for external access to Microsoft Outlook and Microsoft Exchange folders.</span></span> <span data-ttu-id="f65e4-109">A única entrada dessa pasta é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="f65e4-109">The only entry in this folder is the following:</span></span>

`win32=<path>\ACEEXCH.DLL`

<span data-ttu-id="f65e4-110">O mecanismo de banco de dados do Microsoft Access usa esta configuração para indicar a localização do arquivo Aceexch.dll.</span><span class="sxs-lookup"><span data-stu-id="f65e4-110">The Microsoft Access database engine uses this setting to indicate the location of Aceexch.dll.</span></span> <span data-ttu-id="f65e4-111">O caminho completo é determinado no momento da instalação.</span><span class="sxs-lookup"><span data-stu-id="f65e4-111">The full path is determined at the time of installation.</span></span> <span data-ttu-id="f65e4-112">Valores são do tipo REG\_SZ.</span><span class="sxs-lookup"><span data-stu-id="f65e4-112">Values are of type REG\_SZ.</span></span>

<span data-ttu-id="f65e4-p104">Os resultados de usar o formato ISAM do Outlook e do cliente Exchange são iguais. A única diferença é que os dois clientes diferentes usam nomes diferentes para as mesmas colunas. Os dois formatos ISAM foram criados para que o mecanismo de banco de dados do Microsoft Access possa retornar os nomes de coluna no estilo específico que o usuário deseja.</span><span class="sxs-lookup"><span data-stu-id="f65e4-p104">The results of using the Outlook ISAM format and of using the Exchange client ISAM format are similar. The only difference is that the two different clients use different names for the same columns. The two ISAM formats have been created so that the Microsoft Access database engine can return the column names in the particular style that the user desires.</span></span>

## <a name="microsoft-outlook-client-isam-formats"></a><span data-ttu-id="f65e4-116">ISAM Formats para o cliente Microsoft Outlook</span><span class="sxs-lookup"><span data-stu-id="f65e4-116">Microsoft Outlook Client ISAM Formats</span></span>

<span data-ttu-id="f65e4-117">O **mecanismo de conectividade do Access\\ISAM Formats\\Outlook 9.0** pasta contém as entradas a seguir.</span><span class="sxs-lookup"><span data-stu-id="f65e4-117">The **Access Connectivity Engine\\ISAM Formats\\Outlook 9.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f65e4-118">Nome da entrada</span><span class="sxs-lookup"><span data-stu-id="f65e4-118">Entry name</span></span></p></th>
<th><p><span data-ttu-id="f65e4-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="f65e4-119">Type</span></span></p></th>
<th><p><span data-ttu-id="f65e4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f65e4-120">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f65e4-121">Engine</span><span class="sxs-lookup"><span data-stu-id="f65e4-121">Engine</span></span></p></td>
<td><p><span data-ttu-id="f65e4-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f65e4-122">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="f65e4-123">Exchange</span><span class="sxs-lookup"><span data-stu-id="f65e4-123">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f65e4-124">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="f65e4-124">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="f65e4-125">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f65e4-125">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="f65e4-126">Outlook()</span><span class="sxs-lookup"><span data-stu-id="f65e4-126">Outlook()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f65e4-127">CanLink</span><span class="sxs-lookup"><span data-stu-id="f65e4-127">CanLink</span></span></p></td>
<td><p><span data-ttu-id="f65e4-128">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="f65e4-128">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="f65e4-129">01</span><span class="sxs-lookup"><span data-stu-id="f65e4-129">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f65e4-130">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="f65e4-130">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="f65e4-131">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="f65e4-131">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="f65e4-132">00</span><span class="sxs-lookup"><span data-stu-id="f65e4-132">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f65e4-133">IsamType</span><span class="sxs-lookup"><span data-stu-id="f65e4-133">IsamType</span></span></p></td>
<td><p><span data-ttu-id="f65e4-134">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="f65e4-134">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="f65e4-135">3</span><span class="sxs-lookup"><span data-stu-id="f65e4-135">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f65e4-136">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="f65e4-136">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="f65e4-137">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="f65e4-137">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="f65e4-138">00</span><span class="sxs-lookup"><span data-stu-id="f65e4-138">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f65e4-139">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="f65e4-139">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="f65e4-140">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="f65e4-140">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="f65e4-141">00</span><span class="sxs-lookup"><span data-stu-id="f65e4-141">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f65e4-142">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="f65e4-142">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="f65e4-143">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="f65e4-143">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="f65e4-144">01</span><span class="sxs-lookup"><span data-stu-id="f65e4-144">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="f65e4-145">Ao alterar as configurações do Registro do Windows, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="f65e4-145">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="microsoft-exchange-client-isam-formats"></a><span data-ttu-id="f65e4-146">ISAM Formats para cliente Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="f65e4-146">Microsoft Exchange Client ISAM Formats</span></span>

<span data-ttu-id="f65e4-147">O **mecanismo de conectividade do Access\\ISAM Formats\\Exchange 4.0** pasta contém as entradas a seguir.</span><span class="sxs-lookup"><span data-stu-id="f65e4-147">The **Access Connectivity Engine\\ISAM Formats\\Exchange 4.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f65e4-148">Nome da entrada</span><span class="sxs-lookup"><span data-stu-id="f65e4-148">Entry name</span></span></p></th>
<th><p><span data-ttu-id="f65e4-149">Tipo</span><span class="sxs-lookup"><span data-stu-id="f65e4-149">Type</span></span></p></th>
<th><p><span data-ttu-id="f65e4-150">Valor</span><span class="sxs-lookup"><span data-stu-id="f65e4-150">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f65e4-151">Engine</span><span class="sxs-lookup"><span data-stu-id="f65e4-151">Engine</span></span></p></td>
<td><p><span data-ttu-id="f65e4-152">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f65e4-152">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="f65e4-153">Exchange</span><span class="sxs-lookup"><span data-stu-id="f65e4-153">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f65e4-154">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="f65e4-154">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="f65e4-155">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f65e4-155">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="f65e4-156">Exchange()</span><span class="sxs-lookup"><span data-stu-id="f65e4-156">Exchange()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f65e4-157">CanLink</span><span class="sxs-lookup"><span data-stu-id="f65e4-157">CanLink</span></span></p></td>
<td><p><span data-ttu-id="f65e4-158">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="f65e4-158">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="f65e4-159">01</span><span class="sxs-lookup"><span data-stu-id="f65e4-159">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f65e4-160">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="f65e4-160">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="f65e4-161">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="f65e4-161">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="f65e4-162">00</span><span class="sxs-lookup"><span data-stu-id="f65e4-162">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f65e4-163">IsamType</span><span class="sxs-lookup"><span data-stu-id="f65e4-163">IsamType</span></span></p></td>
<td><p><span data-ttu-id="f65e4-164">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="f65e4-164">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="f65e4-165">3</span><span class="sxs-lookup"><span data-stu-id="f65e4-165">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f65e4-166">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="f65e4-166">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="f65e4-167">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="f65e4-167">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="f65e4-168">00</span><span class="sxs-lookup"><span data-stu-id="f65e4-168">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f65e4-169">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="f65e4-169">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="f65e4-170">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="f65e4-170">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="f65e4-171">00</span><span class="sxs-lookup"><span data-stu-id="f65e4-171">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f65e4-172">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="f65e4-172">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="f65e4-173">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="f65e4-173">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="f65e4-174">01</span><span class="sxs-lookup"><span data-stu-id="f65e4-174">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="f65e4-175">Ao alterar as configurações do Registro do Windows, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="f65e4-175">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a><span data-ttu-id="f65e4-176">Personalizando o arquivo Schema.ini para dados do Outlook e do Exchange</span><span class="sxs-lookup"><span data-stu-id="f65e4-176">Customizing the Schema.ini File for Outlook and Exchange Data</span></span>

<span data-ttu-id="f65e4-p105">O arquivo Schema.ini é usado pelo ISAM do Outlook e do Exchange praticamente da mesma maneira que é usado pelo ISAM de texto. O Schema.ini contém informações específicas da fonte de dados: como os dados são formatados e os nomes das colunas que devem ser acessadas.</span><span class="sxs-lookup"><span data-stu-id="f65e4-p105">The Schema.ini file is used by the Outlook and Exchange ISAM in much the same way that it is used by the Text ISAM. Schema.ini contains the specifics of a data source: how the data is formatted, and the names of columns that should be accessed.</span></span>

<span data-ttu-id="f65e4-p106">Não é necessário modificar o arquivo Schema.ini para ler, importar ou exportar dados do Outlook e do Exchange. Várias das configurações internas do arquivo Schema.ini do Outlook e do Exchange são específicas das tags internas que o MAPI exige. Você não deve tentar modificar os valores dessas tags.</span><span class="sxs-lookup"><span data-stu-id="f65e4-p106">It is not necessary to modify the Schema.ini file before data can be read, imported, or exported for Outlook and Exchange. Many of the settings inside the Schema.ini file for Outlook and Exchange are specific to internal tags that MAPI requires. You should not attempt to modify those tag values.</span></span>

