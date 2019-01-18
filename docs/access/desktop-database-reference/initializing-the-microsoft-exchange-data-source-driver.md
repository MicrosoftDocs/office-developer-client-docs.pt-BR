---
title: Inicializando o driver de fonte de dados do Microsoft Exchange
TOCTitle: Initializing the Microsoft Exchange Data Source driver
ms:assetid: cf87a746-f846-1a01-f4ec-20a25e335193
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834677(v=office.15)
ms:contentKeyID: 48547810
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032667
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b3460786785ae7b21184b6d96384ecc59e89d287
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704158"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a><span data-ttu-id="13eae-102">Inicializando o driver de fonte de dados do Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="13eae-102">Initializing the Microsoft Exchange Data Source driver</span></span>

<span data-ttu-id="13eae-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="13eae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="13eae-104">Quando você instala o driver de fonte de dados do Microsoft Exchange, o programa de instalação grava um conjunto de valores padrão para o registro do Microsoft Windows nas subchaves mecanismos e ISAM Formats.</span><span class="sxs-lookup"><span data-stu-id="13eae-104">When you install the Microsoft Exchange Data Source driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="13eae-105">Você não deve modificar essas configurações diretamente; use o programa de instalação de seu aplicativo para adicionar, remover ou alterar essas configurações.</span><span class="sxs-lookup"><span data-stu-id="13eae-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="13eae-106">As seções a seguir descrevem a inicialização e as configurações do ISAM Format no driver de fonte de dados do Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="13eae-106">The following sections describe initialization and ISAM Format settings for the Microsoft Exchange Data Source driver.</span></span>

## <a name="microsoft-exchange-data-source-initialization-settings"></a><span data-ttu-id="13eae-107">Configurações de inicialização da fonte de dados do Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="13eae-107">Microsoft Exchange data source initialization settings</span></span>

<span data-ttu-id="13eae-108">O **mecanismo de conectividade do Access\\mecanismos\\Exchange** pasta inclui configurações de inicialização para o driver Aceexch.dll, usada para acesso externo às pastas do Microsoft Outlook e Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="13eae-108">The **Access Connectivity Engine\\Engines\\Exchange** folder includes initialization settings for the Aceexch.dll driver, used for external access to Microsoft Outlook and Microsoft Exchange folders.</span></span> <span data-ttu-id="13eae-109">A única entrada dessa pasta é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="13eae-109">The only entry in this folder is the following:</span></span>

`win32=<path>\ACEEXCH.DLL`

<span data-ttu-id="13eae-110">O mecanismo de banco de dados do Microsoft Access usa esta configuração para indicar a localização do arquivo Aceexch.dll.</span><span class="sxs-lookup"><span data-stu-id="13eae-110">The Microsoft Access database engine uses this setting to indicate the location of Aceexch.dll.</span></span> <span data-ttu-id="13eae-111">O caminho completo é determinado no momento da instalação.</span><span class="sxs-lookup"><span data-stu-id="13eae-111">The full path is determined at the time of installation.</span></span> <span data-ttu-id="13eae-112">Valores são do tipo REG\_SZ.</span><span class="sxs-lookup"><span data-stu-id="13eae-112">Values are of type REG\_SZ.</span></span>

<span data-ttu-id="13eae-p104">Os resultados de usar o formato ISAM do Outlook e do cliente Exchange são iguais. A única diferença é que os dois clientes diferentes usam nomes diferentes para as mesmas colunas. Os dois formatos ISAM foram criados para que o mecanismo de banco de dados do Microsoft Access possa retornar os nomes de coluna no estilo específico que o usuário deseja.</span><span class="sxs-lookup"><span data-stu-id="13eae-p104">The results of using the Outlook ISAM format and of using the Exchange client ISAM format are similar. The only difference is that the two different clients use different names for the same columns. The two ISAM formats have been created so that the Microsoft Access database engine can return the column names in the particular style that the user desires.</span></span>

## <a name="microsoft-outlook-client-isam-formats"></a><span data-ttu-id="13eae-116">ISAM formats do cliente do Microsoft Outlook</span><span class="sxs-lookup"><span data-stu-id="13eae-116">Microsoft Outlook client ISAM formats</span></span>

<span data-ttu-id="13eae-117">O **mecanismo de conectividade do Access\\ISAM Formats\\Outlook 9.0** pasta contém as entradas a seguir.</span><span class="sxs-lookup"><span data-stu-id="13eae-117">The **Access Connectivity Engine\\ISAM Formats\\Outlook 9.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="13eae-118">Nome da entrada</span><span class="sxs-lookup"><span data-stu-id="13eae-118">Entry name</span></span></p></th>
<th><p><span data-ttu-id="13eae-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="13eae-119">Type</span></span></p></th>
<th><p><span data-ttu-id="13eae-120">Valor</span><span class="sxs-lookup"><span data-stu-id="13eae-120">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13eae-121">Engine</span><span class="sxs-lookup"><span data-stu-id="13eae-121">Engine</span></span></p></td>
<td><p><span data-ttu-id="13eae-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="13eae-122">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="13eae-123">Exchange</span><span class="sxs-lookup"><span data-stu-id="13eae-123">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13eae-124">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="13eae-124">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="13eae-125">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="13eae-125">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="13eae-126">Outlook()</span><span class="sxs-lookup"><span data-stu-id="13eae-126">Outlook()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13eae-127">CanLink</span><span class="sxs-lookup"><span data-stu-id="13eae-127">CanLink</span></span></p></td>
<td><p><span data-ttu-id="13eae-128">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13eae-128">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13eae-129">01</span><span class="sxs-lookup"><span data-stu-id="13eae-129">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13eae-130">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="13eae-130">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="13eae-131">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13eae-131">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13eae-132">00</span><span class="sxs-lookup"><span data-stu-id="13eae-132">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13eae-133">IsamType</span><span class="sxs-lookup"><span data-stu-id="13eae-133">IsamType</span></span></p></td>
<td><p><span data-ttu-id="13eae-134">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="13eae-134">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="13eae-135">3</span><span class="sxs-lookup"><span data-stu-id="13eae-135">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13eae-136">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="13eae-136">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="13eae-137">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13eae-137">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13eae-138">00</span><span class="sxs-lookup"><span data-stu-id="13eae-138">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13eae-139">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="13eae-139">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="13eae-140">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13eae-140">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13eae-141">00</span><span class="sxs-lookup"><span data-stu-id="13eae-141">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13eae-142">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="13eae-142">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="13eae-143">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13eae-143">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13eae-144">01</span><span class="sxs-lookup"><span data-stu-id="13eae-144">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="13eae-145">Ao alterar as configurações do Registro do Windows, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="13eae-145">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="microsoft-exchange-client-isam-formats"></a><span data-ttu-id="13eae-146">ISAM formats do cliente do Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="13eae-146">Microsoft Exchange client ISAM formats</span></span>

<span data-ttu-id="13eae-147">O **mecanismo de conectividade do Access\\ISAM Formats\\Exchange 4.0** pasta contém as entradas a seguir.</span><span class="sxs-lookup"><span data-stu-id="13eae-147">The **Access Connectivity Engine\\ISAM Formats\\Exchange 4.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="13eae-148">Nome da entrada</span><span class="sxs-lookup"><span data-stu-id="13eae-148">Entry name</span></span></p></th>
<th><p><span data-ttu-id="13eae-149">Tipo</span><span class="sxs-lookup"><span data-stu-id="13eae-149">Type</span></span></p></th>
<th><p><span data-ttu-id="13eae-150">Valor</span><span class="sxs-lookup"><span data-stu-id="13eae-150">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13eae-151">Engine</span><span class="sxs-lookup"><span data-stu-id="13eae-151">Engine</span></span></p></td>
<td><p><span data-ttu-id="13eae-152">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="13eae-152">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="13eae-153">Exchange</span><span class="sxs-lookup"><span data-stu-id="13eae-153">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13eae-154">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="13eae-154">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="13eae-155">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="13eae-155">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="13eae-156">Exchange()</span><span class="sxs-lookup"><span data-stu-id="13eae-156">Exchange()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13eae-157">CanLink</span><span class="sxs-lookup"><span data-stu-id="13eae-157">CanLink</span></span></p></td>
<td><p><span data-ttu-id="13eae-158">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13eae-158">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13eae-159">01</span><span class="sxs-lookup"><span data-stu-id="13eae-159">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13eae-160">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="13eae-160">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="13eae-161">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13eae-161">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13eae-162">00</span><span class="sxs-lookup"><span data-stu-id="13eae-162">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13eae-163">IsamType</span><span class="sxs-lookup"><span data-stu-id="13eae-163">IsamType</span></span></p></td>
<td><p><span data-ttu-id="13eae-164">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="13eae-164">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="13eae-165">3</span><span class="sxs-lookup"><span data-stu-id="13eae-165">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13eae-166">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="13eae-166">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="13eae-167">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13eae-167">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13eae-168">00</span><span class="sxs-lookup"><span data-stu-id="13eae-168">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13eae-169">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="13eae-169">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="13eae-170">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13eae-170">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13eae-171">00</span><span class="sxs-lookup"><span data-stu-id="13eae-171">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13eae-172">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="13eae-172">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="13eae-173">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13eae-173">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13eae-174">01</span><span class="sxs-lookup"><span data-stu-id="13eae-174">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="13eae-175">Ao alterar as configurações do Registro do Windows, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="13eae-175">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a><span data-ttu-id="13eae-176">Personalizando o arquivo Schema ini para dados do Outlook e do Exchange</span><span class="sxs-lookup"><span data-stu-id="13eae-176">Customizing the Schema.ini file for Outlook and Exchange data</span></span>

<span data-ttu-id="13eae-p105">O arquivo Schema.ini é usado pelo ISAM do Outlook e do Exchange praticamente da mesma maneira que é usado pelo ISAM de texto. O Schema.ini contém informações específicas da fonte de dados: como os dados são formatados e os nomes das colunas que devem ser acessadas.</span><span class="sxs-lookup"><span data-stu-id="13eae-p105">The Schema.ini file is used by the Outlook and Exchange ISAM in much the same way that it is used by the Text ISAM. Schema.ini contains the specifics of a data source: how the data is formatted, and the names of columns that should be accessed.</span></span>

<span data-ttu-id="13eae-p106">Não é necessário modificar o arquivo Schema.ini para ler, importar ou exportar dados do Outlook e do Exchange. Várias das configurações internas do arquivo Schema.ini do Outlook e do Exchange são específicas das tags internas que o MAPI exige. Você não deve tentar modificar os valores dessas tags.</span><span class="sxs-lookup"><span data-stu-id="13eae-p106">It is not necessary to modify the Schema.ini file before data can be read, imported, or exported for Outlook and Exchange. Many of the settings inside the Schema.ini file for Outlook and Exchange are specific to internal tags that MAPI requires. You should not attempt to modify those tag values.</span></span>

