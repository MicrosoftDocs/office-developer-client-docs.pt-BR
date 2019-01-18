---
title: Inicialização do driver do Microsoft Excel
TOCTitle: Initializing the Microsoft Excel driver
ms:assetid: 06c7f823-8e74-0811-cc00-e6b32075ef11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844939(v=office.15)
ms:contentKeyID: 48543054
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032159
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 12fb79f459024ed113007e6f764945ca9564cb3c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712929"
---
# <a name="initializing-the-microsoft-excel-driver"></a><span data-ttu-id="7d06d-102">Inicialização do driver do Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="7d06d-102">Initializing the Microsoft Excel driver</span></span>

<span data-ttu-id="7d06d-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d06d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7d06d-104">Quando você instala o driver do Excel, o programa de instalação grava um conjunto de valores padrão no registro do Windows nas subchaves mecanismos e ISAM Formats.</span><span class="sxs-lookup"><span data-stu-id="7d06d-104">When you install the Excel driver, the Setup program writes a set of default values to the Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="7d06d-105">Você não deve modificar essas configurações diretamente; use o programa de instalação de seu aplicativo para adicionar, remover ou alterar essas configurações.</span><span class="sxs-lookup"><span data-stu-id="7d06d-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="7d06d-106">As seções a seguir descrevem a inicialização e as configurações do ISAM Format no driver de banco de dados do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="7d06d-106">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="excel-initialization-settings"></a><span data-ttu-id="7d06d-107">Configurações de inicialização do Excel</span><span class="sxs-lookup"><span data-stu-id="7d06d-107">Excel initialization settings</span></span>

<span data-ttu-id="7d06d-108">O **mecanismo de conectividade do Access\\mecanismos\\Excel** pasta inclui configurações de inicialização para o driver Aceexcl.dll, usada para acesso externo às planilhas do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="7d06d-108">The **Access Connectivity Engine\\Engines\\Excel** folder includes initialization settings for the Aceexcl.dll driver, used for external access to Microsoft Excel worksheets.</span></span> <span data-ttu-id="7d06d-109">As configurações normais das entradas nessa pasta são mostradas no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="7d06d-109">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

<span data-ttu-id="7d06d-110">O mecanismo de banco de dados do Microsoft Access usa as entradas da pasta do Excel da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7d06d-110">The Microsoft Access database engine uses the Excel folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d06d-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="7d06d-111">Entry</span></span></p></th>
<th><p><span data-ttu-id="7d06d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d06d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d06d-113">Win32</span><span class="sxs-lookup"><span data-stu-id="7d06d-113">win32</span></span></p></td>
<td><p><span data-ttu-id="7d06d-p103">A localização do arquivo msexcl40. O caminho completo é determinado no momento da instalação. Os valores são do tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="7d06d-p103">The location of msexcl40.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d06d-117">Registo TypeGuessRows</span><span class="sxs-lookup"><span data-stu-id="7d06d-117">TypeGuessRows</span></span></p></td>
<td><p><span data-ttu-id="7d06d-118">O número de linhas a serem verificadas para o tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7d06d-118">The number of rows to be checked for the data type.</span></span> <span data-ttu-id="7d06d-119">O tipo de dados é determinado dado o número máximo de tipos de dados encontrados.</span><span class="sxs-lookup"><span data-stu-id="7d06d-119">The data type is determined given the maximum number of kinds of data found.</span></span> <span data-ttu-id="7d06d-120">Se houver uma ligação, o tipo de dados é determinado na seguinte ordem: número, moeda, data, texto, Boolean.</span><span class="sxs-lookup"><span data-stu-id="7d06d-120">If there is a tie, the data type is determined in the following order: Number, Currency, Date, Text, Boolean.</span></span> <span data-ttu-id="7d06d-121">Se forem encontrados dados que não coincide com o tipo de dados avaliado para a coluna, ele é retornado como um valor <strong>Nulo</strong> .</span><span class="sxs-lookup"><span data-stu-id="7d06d-121">If data is encountered that does not match the data type guessed for the column, it is returned as a <strong>Null</strong> value.</span></span> <span data-ttu-id="7d06d-122">Na importação, se uma coluna tiver mistos tipos de dados, toda a coluna será convertida de acordo com a configuração ImportMixedTypes.</span><span class="sxs-lookup"><span data-stu-id="7d06d-122">On import, if a column has mixed data types, the entire column will be cast according to the ImportMixedTypes setting.</span></span> <span data-ttu-id="7d06d-123">O número padrão de linhas a serem verificadas é 8.</span><span class="sxs-lookup"><span data-stu-id="7d06d-123">The default number of rows to be checked is 8.</span></span> <span data-ttu-id="7d06d-124">Os valores são do tipo REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="7d06d-124">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d06d-125">ImportMixedTypes</span><span class="sxs-lookup"><span data-stu-id="7d06d-125">ImportMixedTypes</span></span></p></td>
<td><p><span data-ttu-id="7d06d-p105">Pode ser definido como MajorityType ou Text. Se for definido como MajorityType, as colunas com tipos de dados mistos serão calculadas conforme o tipo de dados predominante na importação. Se for definido como Text, as colunas de tipos de dados mistos serão calculadas como Text na importação. O padrão é Text. Os valores são do tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="7d06d-p105">Can be set to MajorityType or Text. If set to MajorityType, columns of mixed data types will be cast to the predominate data type on import. If set to Text, columns of mixed data types will be cast to Text on import. The default is Text. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d06d-131">AppendBlankRows</span><span class="sxs-lookup"><span data-stu-id="7d06d-131">AppendBlankRows</span></span></p></td>
<td><p><span data-ttu-id="7d06d-p106">O número de linhas em branco a serem acrescentadas ao final de uma planilha da versão 3.5 ou 4.0 antes da adição de novos dados. Por exemplo, se AppendBlankRows for definido como, o Microsoft Jet acrescentará 4 linhas em branco ao final da planilha antes de acrescentar linhas que contenham dados. Valores inteiros nessa configuração podem variar de 0 a 16; o padrão é 01 (uma linha adicional acrescentada). Os valores são do tipo REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="7d06d-p106">The number of blank rows to be appended to the end of a Version 3.5 or Version 4.0 worksheet before new data is added. For example, if AppendBlankRows is set to 4, Microsoft Jet will append 4 blank rows to the end of the worksheet before appending rows that contain data. Integer values for this setting can range from 0 to 16; the default is 01 (one additional row appended). Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d06d-136">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="7d06d-136">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="7d06d-p107">Um valor binário que indica se a primeira linha da tabela contém nomes de coluna. O valor 01 indica que, durante a importação, os nomes de coluna são extraídos da primeira linha. O valor 00 indica nenhum nome de coluna na primeira linha; os nomes de coluna aparecem como F1, F2, F3 etc. O padrão é 01. Os valores são do tipo REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="7d06d-p107">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row. A value of 00 indicates no column names in the first row; column names appear as F1, F2, F3, and so on. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="7d06d-142">O **mecanismo de conectividade do Access\\mecanismos\\Excel 8.0** pasta contém as entradas a seguir, que se aplicam ao Microsoft Excel 97.</span><span class="sxs-lookup"><span data-stu-id="7d06d-142">The **Access Connectivity Engine\\Engines\\Excel 8.0** folder contains the following entries, which apply to Microsoft Excel 97.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d06d-143">Nome da entrada</span><span class="sxs-lookup"><span data-stu-id="7d06d-143">Entry name</span></span></p></th>
<th><p><span data-ttu-id="7d06d-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="7d06d-144">Type</span></span></p></th>
<th><p><span data-ttu-id="7d06d-145">Valor</span><span class="sxs-lookup"><span data-stu-id="7d06d-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d06d-146">Engine</span><span class="sxs-lookup"><span data-stu-id="7d06d-146">Engine</span></span></p></td>
<td><p><span data-ttu-id="7d06d-147">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="7d06d-147">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="7d06d-148">Excel</span><span class="sxs-lookup"><span data-stu-id="7d06d-148">Excel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d06d-149">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="7d06d-149">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="7d06d-150">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="7d06d-150">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="7d06d-151">Microsoft Excel 97-2000 (\*.xls)</span><span class="sxs-lookup"><span data-stu-id="7d06d-151">Microsoft Excel 97-2000 (\*.xls)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d06d-152">CanLink</span><span class="sxs-lookup"><span data-stu-id="7d06d-152">CanLink</span></span></p></td>
<td><p><span data-ttu-id="7d06d-153">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="7d06d-153">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="7d06d-154">01</span><span class="sxs-lookup"><span data-stu-id="7d06d-154">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d06d-155">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="7d06d-155">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="7d06d-156">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="7d06d-156">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="7d06d-157">00</span><span class="sxs-lookup"><span data-stu-id="7d06d-157">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d06d-158">IsamType</span><span class="sxs-lookup"><span data-stu-id="7d06d-158">IsamType</span></span></p></td>
<td><p><span data-ttu-id="7d06d-159">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="7d06d-159">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="7d06d-160">1</span><span class="sxs-lookup"><span data-stu-id="7d06d-160">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d06d-161">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="7d06d-161">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="7d06d-162">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="7d06d-162">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="7d06d-163">00</span><span class="sxs-lookup"><span data-stu-id="7d06d-163">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d06d-164">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="7d06d-164">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="7d06d-165">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="7d06d-165">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="7d06d-166">01</span><span class="sxs-lookup"><span data-stu-id="7d06d-166">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d06d-167">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="7d06d-167">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="7d06d-168">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="7d06d-168">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="7d06d-p108">Exportar dados do banco de dados atual para um arquivo do Microsoft Excel 97. Esse processo substituirá os dados quando exportados para um arquivo já existente.</span><span class="sxs-lookup"><span data-stu-id="7d06d-p108">Export data from the current database into a Microsoft Excel 97 file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d06d-171">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="7d06d-171">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="7d06d-172">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="7d06d-172">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="7d06d-173">01</span><span class="sxs-lookup"><span data-stu-id="7d06d-173">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="7d06d-174">Ao alterar as configurações do Registro do Windows, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="7d06d-174">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d06d-175">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d06d-175">See also</span></span>

- [<span data-ttu-id="7d06d-176">Usando a configuração de registo TypeGuessRows para o Driver do Excel</span><span class="sxs-lookup"><span data-stu-id="7d06d-176">Using the TypeGuessRows setting for Excel Driver</span></span>](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)
