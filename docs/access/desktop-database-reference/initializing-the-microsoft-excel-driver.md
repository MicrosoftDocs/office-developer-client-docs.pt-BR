---
title: Inicializando o driver do Microsoft Excel
TOCTitle: Initializing the Microsoft Excel Driver
ms:assetid: 06c7f823-8e74-0811-cc00-e6b32075ef11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844939(v=office.15)
ms:contentKeyID: 48543054
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032159
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7c9a3282f3bb508a4c68ecbd3f2c0465cfee9bac
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603095"
---
# <a name="initializing-the-microsoft-excel-driver"></a><span data-ttu-id="75ed4-102">Inicializando o driver do Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="75ed4-102">Initializing the Microsoft Excel Driver</span></span>


<span data-ttu-id="75ed4-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="75ed4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="75ed4-104"><<<<<<< Cabeça quando você instalar o driver do Microsoft® Excel, o programa de instalação grava um conjunto de valores padrão para o registro do Microsoft Windows® nas subchaves mecanismos e ISAM Formats.</span><span class="sxs-lookup"><span data-stu-id="75ed4-104"><<<<<<< HEAD When you install the Microsoft® Excel driver, the Setup program writes a set of default values to the Microsoft Windows® Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="75ed4-105">Você não deve modificar essas configurações diretamente; use o programa de instalação de seu aplicativo para adicionar, remover ou alterar essas configurações.</span><span class="sxs-lookup"><span data-stu-id="75ed4-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="75ed4-106">As seções a seguir descrevem a inicialização e as configurações do ISAM Format no driver de banco de dados do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="75ed4-106">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="microsoft-excel-initialization-settings"></a><span data-ttu-id="75ed4-107">Configurações de inicialização do Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="75ed4-107">Microsoft Excel Initialization Settings</span></span>
<span data-ttu-id="75ed4-108">=== Quando você instala o driver do Excel, o programa de instalação grava um conjunto de valores padrão no registro do Windows nas subchaves mecanismos e ISAM Formats.</span><span class="sxs-lookup"><span data-stu-id="75ed4-108">======= When you install the Excel driver, the Setup program writes a set of default values to the Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="75ed4-109">Você não deve modificar essas configurações diretamente; use o programa de instalação de seu aplicativo para adicionar, remover ou alterar essas configurações.</span><span class="sxs-lookup"><span data-stu-id="75ed4-109">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="75ed4-110">As seções a seguir descrevem a inicialização e as configurações do ISAM Format no driver de banco de dados do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="75ed4-110">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="excel-initialization-settings"></a><span data-ttu-id="75ed4-111">Configurações de inicialização do Excel</span><span class="sxs-lookup"><span data-stu-id="75ed4-111">Excel Initialization Settings</span></span>
>>>>>>> <span data-ttu-id="75ed4-112">mestre</span><span class="sxs-lookup"><span data-stu-id="75ed4-112">master</span></span>

<span data-ttu-id="75ed4-113">O **mecanismo de conectividade do Access\\mecanismos\\Excel** pasta inclui configurações de inicialização para o driver Aceexcl.dll, usada para acesso externo às planilhas do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="75ed4-113">The **Access Connectivity Engine\\Engines\\Excel** folder includes initialization settings for the Aceexcl.dll driver, used for external access to Microsoft Excel worksheets.</span></span> <span data-ttu-id="75ed4-114">As configurações normais das entradas nessa pasta são mostradas no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="75ed4-114">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

<span data-ttu-id="75ed4-115">O mecanismo de banco de dados do Microsoft Access usa as entradas da pasta do Excel da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="75ed4-115">The Microsoft Access database engine uses the Excel folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75ed4-116">Entrada</span><span class="sxs-lookup"><span data-stu-id="75ed4-116">Entry</span></span></p></th>
<th><p><span data-ttu-id="75ed4-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="75ed4-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75ed4-118">Win32</span><span class="sxs-lookup"><span data-stu-id="75ed4-118">win32</span></span></p></td>
<td><p><span data-ttu-id="75ed4-p104">A localização do arquivo msexcl40. O caminho completo é determinado no momento da instalação. Os valores são do tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="75ed4-p104">The location of msexcl40.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ed4-122">Registo TypeGuessRows</span><span class="sxs-lookup"><span data-stu-id="75ed4-122">TypeGuessRows</span></span></p></td>
<td><p><span data-ttu-id="75ed4-123">O número de linhas a serem verificadas para o tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="75ed4-123">The number of rows to be checked for the data type.</span></span> <span data-ttu-id="75ed4-124">O tipo de dados é determinado dado o número máximo de tipos de dados encontrados.</span><span class="sxs-lookup"><span data-stu-id="75ed4-124">The data type is determined given the maximum number of kinds of data found.</span></span> <span data-ttu-id="75ed4-125">Se houver uma ligação, o tipo de dados é determinado na seguinte ordem: número, moeda, data, texto, Boolean.</span><span class="sxs-lookup"><span data-stu-id="75ed4-125">If there is a tie, the data type is determined in the following order: Number, Currency, Date, Text, Boolean.</span></span> <span data-ttu-id="75ed4-126">Se forem encontrados dados que não coincide com o tipo de dados avaliado para a coluna, ele é retornado como um valor <strong>Nulo</strong> .</span><span class="sxs-lookup"><span data-stu-id="75ed4-126">If data is encountered that does not match the data type guessed for the column, it is returned as a <strong>Null</strong> value.</span></span> <span data-ttu-id="75ed4-127">Na importação, se uma coluna tiver mistos tipos de dados, toda a coluna será convertida de acordo com a configuração ImportMixedTypes.</span><span class="sxs-lookup"><span data-stu-id="75ed4-127">On import, if a column has mixed data types, the entire column will be cast according to the ImportMixedTypes setting.</span></span> <span data-ttu-id="75ed4-128">O número padrão de linhas a serem verificadas é 8.</span><span class="sxs-lookup"><span data-stu-id="75ed4-128">The default number of rows to be checked is 8.</span></span> <span data-ttu-id="75ed4-129">Os valores são do tipo REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="75ed4-129">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75ed4-130">ImportMixedTypes</span><span class="sxs-lookup"><span data-stu-id="75ed4-130">ImportMixedTypes</span></span></p></td>
<td><p><span data-ttu-id="75ed4-p106">Pode ser definido como MajorityType ou Text. Se for definido como MajorityType, as colunas com tipos de dados mistos serão calculadas conforme o tipo de dados predominante na importação. Se for definido como Text, as colunas de tipos de dados mistos serão calculadas como Text na importação. O padrão é Text. Os valores são do tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="75ed4-p106">Can be set to MajorityType or Text. If set to MajorityType, columns of mixed data types will be cast to the predominate data type on import. If set to Text, columns of mixed data types will be cast to Text on import. The default is Text. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ed4-136">AppendBlankRows</span><span class="sxs-lookup"><span data-stu-id="75ed4-136">AppendBlankRows</span></span></p></td>
<td><p><span data-ttu-id="75ed4-p107">O número de linhas em branco a serem acrescentadas ao final de uma planilha da versão 3.5 ou 4.0 antes da adição de novos dados. Por exemplo, se AppendBlankRows for definido como, o Microsoft Jet acrescentará 4 linhas em branco ao final da planilha antes de acrescentar linhas que contenham dados. Valores inteiros nessa configuração podem variar de 0 a 16; o padrão é 01 (uma linha adicional acrescentada). Os valores são do tipo REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="75ed4-p107">The number of blank rows to be appended to the end of a Version 3.5 or Version 4.0 worksheet before new data is added. For example, if AppendBlankRows is set to 4, Microsoft Jet will append 4 blank rows to the end of the worksheet before appending rows that contain data. Integer values for this setting can range from 0 to 16; the default is 01 (one additional row appended). Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75ed4-141">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="75ed4-141">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="75ed4-p108">Um valor binário que indica se a primeira linha da tabela contém nomes de coluna. O valor 01 indica que, durante a importação, os nomes de coluna são extraídos da primeira linha. O valor 00 indica nenhum nome de coluna na primeira linha; os nomes de coluna aparecem como F1, F2, F3 etc. O padrão é 01. Os valores são do tipo REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="75ed4-p108">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row. A value of 00 indicates no column names in the first row; column names appear as F1, F2, F3, and so on. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="75ed4-147">O **mecanismo de conectividade do Access\\mecanismos\\Excel 8.0** pasta contém as entradas a seguir, que se aplicam ao Microsoft Excel 97.</span><span class="sxs-lookup"><span data-stu-id="75ed4-147">The **Access Connectivity Engine\\Engines\\Excel 8.0** folder contains the following entries, which apply to Microsoft Excel 97.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75ed4-148">Nome da entrada</span><span class="sxs-lookup"><span data-stu-id="75ed4-148">Entry name</span></span></p></th>
<th><p><span data-ttu-id="75ed4-149">Tipo</span><span class="sxs-lookup"><span data-stu-id="75ed4-149">Type</span></span></p></th>
<th><p><span data-ttu-id="75ed4-150">Valor</span><span class="sxs-lookup"><span data-stu-id="75ed4-150">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75ed4-151">Engine</span><span class="sxs-lookup"><span data-stu-id="75ed4-151">Engine</span></span></p></td>
<td><p><span data-ttu-id="75ed4-152">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="75ed4-152">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="75ed4-153">Excel</span><span class="sxs-lookup"><span data-stu-id="75ed4-153">Excel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ed4-154">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="75ed4-154">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="75ed4-155">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="75ed4-155">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="75ed4-156">Microsoft Excel 97-2000 (\*.xls)</span><span class="sxs-lookup"><span data-stu-id="75ed4-156">Microsoft Excel 97-2000 (\*.xls)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75ed4-157">CanLink</span><span class="sxs-lookup"><span data-stu-id="75ed4-157">CanLink</span></span></p></td>
<td><p><span data-ttu-id="75ed4-158">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="75ed4-158">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="75ed4-159">01</span><span class="sxs-lookup"><span data-stu-id="75ed4-159">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ed4-160">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="75ed4-160">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="75ed4-161">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="75ed4-161">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="75ed4-162">00</span><span class="sxs-lookup"><span data-stu-id="75ed4-162">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75ed4-163">IsamType</span><span class="sxs-lookup"><span data-stu-id="75ed4-163">IsamType</span></span></p></td>
<td><p><span data-ttu-id="75ed4-164">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="75ed4-164">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="75ed4-165">1</span><span class="sxs-lookup"><span data-stu-id="75ed4-165">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ed4-166">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="75ed4-166">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="75ed4-167">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="75ed4-167">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="75ed4-168">00</span><span class="sxs-lookup"><span data-stu-id="75ed4-168">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75ed4-169">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="75ed4-169">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="75ed4-170">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="75ed4-170">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="75ed4-171">01</span><span class="sxs-lookup"><span data-stu-id="75ed4-171">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ed4-172">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="75ed4-172">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="75ed4-173">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="75ed4-173">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="75ed4-p109">Exportar dados do banco de dados atual para um arquivo do Microsoft Excel 97. Esse processo substituirá os dados quando exportados para um arquivo já existente.</span><span class="sxs-lookup"><span data-stu-id="75ed4-p109">Export data from the current database into a Microsoft Excel 97 file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75ed4-176">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="75ed4-176">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="75ed4-177">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="75ed4-177">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="75ed4-178">01</span><span class="sxs-lookup"><span data-stu-id="75ed4-178">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="75ed4-179">Ao alterar as configurações do Registro do Windows, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="75ed4-179">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

<span data-ttu-id="75ed4-180"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="75ed4-180"><<<<<<< HEAD</span></span>

=======
## <a name="see-also"></a><span data-ttu-id="75ed4-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="75ed4-181">See also</span></span>

[<span data-ttu-id="75ed4-182">Usando a configuração de registo TypeGuessRows para o Driver do Excel</span><span class="sxs-lookup"><span data-stu-id="75ed4-182">Using the TypeGuessRows setting for Excel Driver</span></span>](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)
>>>>>>> <span data-ttu-id="75ed4-183">mestre</span><span class="sxs-lookup"><span data-stu-id="75ed4-183">master</span></span>
