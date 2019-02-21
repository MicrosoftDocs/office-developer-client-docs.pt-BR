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
ms.openlocfilehash: cec7890385e5730831cea9241278511d88b6f3a1
ms.sourcegitcommit: 8ead5b5501f59c108cf02969070be21f7fc52467
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/21/2019
ms.locfileid: "30135744"
---
# <a name="initializing-the-microsoft-excel-driver"></a><span data-ttu-id="03321-102">Inicialização do driver do Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="03321-102">Initializing the Microsoft Excel driver</span></span>

<span data-ttu-id="03321-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="03321-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="03321-104">Quando você instala o driver do Excel, o programa de instalação grava um conjunto de valores padrão no registro do Windows nas subchaves Engines e ISAM formats.</span><span class="sxs-lookup"><span data-stu-id="03321-104">When you install the Excel driver, the Setup program writes a set of default values to the Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="03321-105">Você não deve modificar essas configurações diretamente; use o programa de instalação de seu aplicativo para adicionar, remover ou alterar essas configurações.</span><span class="sxs-lookup"><span data-stu-id="03321-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="03321-106">As seções a seguir descrevem a inicialização e as configurações do ISAM Format no driver de banco de dados do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="03321-106">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="excel-initialization-settings"></a><span data-ttu-id="03321-107">Configurações de inicialização do Excel</span><span class="sxs-lookup"><span data-stu-id="03321-107">Excel initialization settings</span></span>

<span data-ttu-id="03321-108">A pasta do **Excel\\mecanismos\\do mecanismo de conectividade do Access** inclui configurações de inicialização para o driver Aceexcl. dll, usado para acesso externo às planilhas do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="03321-108">The **Access Connectivity Engine\\Engines\\Excel** folder includes initialization settings for the Aceexcl.dll driver, used for external access to Microsoft Excel worksheets.</span></span> <span data-ttu-id="03321-109">As configurações normais das entradas nessa pasta são mostradas no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="03321-109">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

<span data-ttu-id="03321-110">O mecanismo de banco de dados do Microsoft Access usa as entradas da pasta do Excel da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="03321-110">The Microsoft Access database engine uses the Excel folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03321-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="03321-111">Entry</span></span></p></th>
<th><p><span data-ttu-id="03321-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="03321-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03321-113">Win</span><span class="sxs-lookup"><span data-stu-id="03321-113">win32</span></span></p></td>
<td><p><span data-ttu-id="03321-p103">A localização do arquivo msexcl40. O caminho completo é determinado no momento da instalação. Os valores são do tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="03321-p103">The location of msexcl40.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03321-117">TypeGuessRows</span><span class="sxs-lookup"><span data-stu-id="03321-117">TypeGuessRows</span></span></p></td>
<td><p><span data-ttu-id="03321-118">O número de linhas a serem verificadas quanto ao tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="03321-118">The number of rows to be checked for the data type.</span></span> <span data-ttu-id="03321-119">O tipo de dados é determinado de acordo com o número máximo de tipos de dados encontrados.</span><span class="sxs-lookup"><span data-stu-id="03321-119">The data type is determined given the maximum number of kinds of data found.</span></span> <span data-ttu-id="03321-120">Se houver um vínculo, o tipo de dados é determinado na seguinte ordem: número, moeda, data, texto, Boolean.</span><span class="sxs-lookup"><span data-stu-id="03321-120">If there is a tie, the data type is determined in the following order: Number, Currency, Date, Text, Boolean.</span></span> <span data-ttu-id="03321-121">Se forem encontrados dados que não correspondem ao tipo de dados adivinhado para a coluna, ele será retornado como um valor <strong>nulo</strong> .</span><span class="sxs-lookup"><span data-stu-id="03321-121">If data is encountered that does not match the data type guessed for the column, it is returned as a <strong>Null</strong> value.</span></span> <span data-ttu-id="03321-122">Na importação, se uma coluna tiver tipos de dados mistos, a coluna inteira será convertida de acordo com a configuração ImportMixedTypes.</span><span class="sxs-lookup"><span data-stu-id="03321-122">On import, if a column has mixed data types, the entire column will be cast according to the ImportMixedTypes setting.</span></span> <span data-ttu-id="03321-123">O número padrão de linhas a serem verificadas é 8.</span><span class="sxs-lookup"><span data-stu-id="03321-123">The default number of rows to be checked is 8.</span></span> <span data-ttu-id="03321-124">Os valores são do tipo REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="03321-124">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03321-125">ImportMixedTypes</span><span class="sxs-lookup"><span data-stu-id="03321-125">ImportMixedTypes</span></span></p></td>
<td><p><span data-ttu-id="03321-p105">Pode ser definido como MajorityType ou Text. Se for definido como MajorityType, as colunas com tipos de dados mistos serão calculadas conforme o tipo de dados predominante na importação. Se for definido como Text, as colunas de tipos de dados mistos serão calculadas como Text na importação. O padrão é Text. Os valores são do tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="03321-p105">Can be set to MajorityType or Text. If set to MajorityType, columns of mixed data types will be cast to the predominate data type on import. If set to Text, columns of mixed data types will be cast to Text on import. The default is Text. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03321-131">AppendBlankRows</span><span class="sxs-lookup"><span data-stu-id="03321-131">AppendBlankRows</span></span></p></td>
<td><p><span data-ttu-id="03321-p106">O número de linhas em branco a serem acrescentadas ao final de uma planilha da versão 3.5 ou 4.0 antes da adição de novos dados. Por exemplo, se AppendBlankRows for definido como, o Microsoft Jet acrescentará 4 linhas em branco ao final da planilha antes de acrescentar linhas que contenham dados. Valores inteiros nessa configuração podem variar de 0 a 16; o padrão é 01 (uma linha adicional acrescentada). Os valores são do tipo REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="03321-p106">The number of blank rows to be appended to the end of a Version 3.5 or Version 4.0 worksheet before new data is added. For example, if AppendBlankRows is set to 4, Microsoft Jet will append 4 blank rows to the end of the worksheet before appending rows that contain data. Integer values for this setting can range from 0 to 16; the default is 01 (one additional row appended). Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03321-136">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="03321-136">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="03321-p107">Um valor binário que indica se a primeira linha da tabela contém nomes de coluna. O valor 01 indica que, durante a importação, os nomes de coluna são extraídos da primeira linha. O valor 00 indica nenhum nome de coluna na primeira linha; os nomes de coluna aparecem como F1, F2, F3 etc. O padrão é 01. Os valores são do tipo REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="03321-p107">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row. A value of 00 indicates no column names in the first row; column names appear as F1, F2, F3, and so on. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="03321-142">A pasta **mecanismos\\\\de mecanismo de conectividade do Microsoft Excel 8,0** contém as entradas a seguir, que se aplicam ao Microsoft Excel 97.</span><span class="sxs-lookup"><span data-stu-id="03321-142">The **Access Connectivity Engine\\Engines\\Excel 8.0** folder contains the following entries, which apply to Microsoft Excel 97.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03321-143">Nome da entrada</span><span class="sxs-lookup"><span data-stu-id="03321-143">Entry name</span></span></p></th>
<th><p><span data-ttu-id="03321-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="03321-144">Type</span></span></p></th>
<th><p><span data-ttu-id="03321-145">Valor</span><span class="sxs-lookup"><span data-stu-id="03321-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03321-146">Engine</span><span class="sxs-lookup"><span data-stu-id="03321-146">Engine</span></span></p></td>
<td><p><span data-ttu-id="03321-147">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="03321-147">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="03321-148">Excel</span><span class="sxs-lookup"><span data-stu-id="03321-148">Excel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03321-149">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="03321-149">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="03321-150">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="03321-150">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="03321-151">Microsoft Excel 97-2000 (\*.xls)</span><span class="sxs-lookup"><span data-stu-id="03321-151">Microsoft Excel 97-2000 (\*.xls)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03321-152">CanVinculo</span><span class="sxs-lookup"><span data-stu-id="03321-152">CanLink</span></span></p></td>
<td><p><span data-ttu-id="03321-153">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="03321-153">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="03321-154">0,01</span><span class="sxs-lookup"><span data-stu-id="03321-154">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03321-155">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="03321-155">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="03321-156">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="03321-156">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="03321-157">00</span><span class="sxs-lookup"><span data-stu-id="03321-157">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03321-158">Isamtype</span><span class="sxs-lookup"><span data-stu-id="03321-158">IsamType</span></span></p></td>
<td><p><span data-ttu-id="03321-159">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="03321-159">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="03321-160">1</span><span class="sxs-lookup"><span data-stu-id="03321-160">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03321-161">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="03321-161">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="03321-162">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="03321-162">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="03321-163">00</span><span class="sxs-lookup"><span data-stu-id="03321-163">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03321-164">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="03321-164">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="03321-165">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="03321-165">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="03321-166">0,01</span><span class="sxs-lookup"><span data-stu-id="03321-166">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03321-167">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="03321-167">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="03321-168">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="03321-168">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="03321-p108">Exportar dados do banco de dados atual para um arquivo do Microsoft Excel 97. Esse processo substituirá os dados quando exportados para um arquivo já existente.</span><span class="sxs-lookup"><span data-stu-id="03321-p108">Export data from the current database into a Microsoft Excel 97 file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03321-171">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="03321-171">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="03321-172">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="03321-172">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="03321-173">0,01</span><span class="sxs-lookup"><span data-stu-id="03321-173">01</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="using-the-typeguessrows-setting-for-excel-driver"></a><span data-ttu-id="03321-174">Usando a configuração TypeGuessRows para o driver do Excel</span><span class="sxs-lookup"><span data-stu-id="03321-174">Using the TypeGuessRows setting for Excel Driver</span></span>
<span data-ttu-id="03321-175">Ao usar o driver do Microsoft Excel, você pode usar o valor de registro **TypeGuessRows** para configurar quantas linhas devem ser verificadas quanto ao tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="03321-175">When you use Microsoft Excel Driver, you can use the **TypeGuessRows** registry value to configure how many rows are to be checked for the data type.</span></span> <span data-ttu-id="03321-176">O valor **TypeGuessRows** está localizado na seguinte subchave do registro:</span><span class="sxs-lookup"><span data-stu-id="03321-176">The **TypeGuessRows** value is located under the following registry subkey:</span></span>

# <a name="office-2016taboffice-2016"></a>[<span data-ttu-id="03321-177">Office 2016</span><span class="sxs-lookup"><span data-stu-id="03321-177">Office 2016</span></span>](#tab/office-2016)

<span data-ttu-id="03321-178">Para uma instalação MSI do Office</span><span class="sxs-lookup"><span data-stu-id="03321-178">For an MSI installation of Office</span></span>

- <span data-ttu-id="03321-179">Para o Office de 32 bits no Windows de 32 bits ou no Office de 64 bits no Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="03321-179">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="03321-180">**Engine\Engines\Excel de conectividade HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access**</span><span class="sxs-lookup"><span data-stu-id="03321-180">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

- <span data-ttu-id="03321-181">Para o Office de 32 bits em Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="03321-181">For 32-bit Office on 64-bit Windows:</span></span>

  <span data-ttu-id="03321-182">**Engine\Engines\Excel de conectividade HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access**</span><span class="sxs-lookup"><span data-stu-id="03321-182">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>
    
<span data-ttu-id="03321-183">Para uma instalação clique para executar do Office</span><span class="sxs-lookup"><span data-stu-id="03321-183">For a Click-to-Run installation of Office</span></span>

- <span data-ttu-id="03321-184">Para o Office de 32 bits no Windows de 32 bits ou no Office de 64 bits no Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="03321-184">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="03321-185">**Engine\Engines\Excel de conectividade HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access**</span><span class="sxs-lookup"><span data-stu-id="03321-185">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

- <span data-ttu-id="03321-186">Para o Office de 32 bits em Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="03321-186">For 32-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="03321-187">**Engine\Engines\Excel de conectividade HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access**</span><span class="sxs-lookup"><span data-stu-id="03321-187">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="03321-188">O número padrão de linhas a serem verificadas é **8** (oito).</span><span class="sxs-lookup"><span data-stu-id="03321-188">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="03321-189">Quando você define o valor de **TypeGuessRows** para **0** (zero), o driver do Excel verifica as primeiras 16.384 linhas para o tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="03321-189">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="03321-190">Se você deseja verificar mais de 16.384 linhas, defina **TypeGuessRows** como um valor que se baseia no intervalo desejado.</span><span class="sxs-lookup"><span data-stu-id="03321-190">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="03321-191">Para verificar todas as linhas, defina **TypeGuessRows** como 1.048.576 (o número máximo de linhas permitido no Excel).</span><span class="sxs-lookup"><span data-stu-id="03321-191">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="03321-192">O tipo de dados é determinado pelo número máximo de tipos de dados que é encontrado.</span><span class="sxs-lookup"><span data-stu-id="03321-192">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="03321-193">Se houver um empate, o tipo de dados será determinado na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="03321-193">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="03321-194">Número</span><span class="sxs-lookup"><span data-stu-id="03321-194">Number</span></span>
- <span data-ttu-id="03321-195">Moeda</span><span class="sxs-lookup"><span data-stu-id="03321-195">Currency</span></span>
- <span data-ttu-id="03321-196">Data</span><span class="sxs-lookup"><span data-stu-id="03321-196">Date</span></span>
- <span data-ttu-id="03321-197">Texto</span><span class="sxs-lookup"><span data-stu-id="03321-197">Text</span></span>
- <span data-ttu-id="03321-198">Booliano</span><span class="sxs-lookup"><span data-stu-id="03321-198">Boolean</span></span>

<span data-ttu-id="03321-199">Se forem encontrados dados que não correspondam ao tipo de dados adivinhados para a coluna, esses dados serão retornados como um valor **nulo** .</span><span class="sxs-lookup"><span data-stu-id="03321-199">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="03321-200">Durante uma importação, se uma coluna tem tipos de dados mistos, toda a coluna é convertida para o tipo de dados definido pela configuração **ImportMixedTypes** .</span><span class="sxs-lookup"><span data-stu-id="03321-200">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

# <a name="office-2013taboffice-2013"></a>[<span data-ttu-id="03321-201">Office 2013</span><span class="sxs-lookup"><span data-stu-id="03321-201">Office 2013</span></span>](#tab/office-2013)

<span data-ttu-id="03321-202">Para o Office de 32 bits no Windows de 32 bits ou no Office de 64 bits no Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="03321-202">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="03321-203">**Engine\Engines\Excel de conectividade HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access**</span><span class="sxs-lookup"><span data-stu-id="03321-203">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="03321-204">Para o Office de 32 bits em Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="03321-204">For 32-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="03321-205">**Engine\Engines\Excel de conectividade HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access**</span><span class="sxs-lookup"><span data-stu-id="03321-205">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="03321-206">O número padrão de linhas a serem verificadas é **8** (oito).</span><span class="sxs-lookup"><span data-stu-id="03321-206">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="03321-207">Quando você define o valor de **TypeGuessRows** para **0** (zero), o driver do Excel verifica as primeiras 16.384 linhas para o tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="03321-207">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="03321-208">Se você deseja verificar mais de 16.384 linhas, defina **TypeGuessRows** como um valor que se baseia no intervalo desejado.</span><span class="sxs-lookup"><span data-stu-id="03321-208">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="03321-209">Para verificar todas as linhas, defina **TypeGuessRows** como 1.048.576 (o número máximo de linhas permitido no Excel).</span><span class="sxs-lookup"><span data-stu-id="03321-209">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="03321-210">O tipo de dados é determinado pelo número máximo de tipos de dados que é encontrado.</span><span class="sxs-lookup"><span data-stu-id="03321-210">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="03321-211">Se houver um empate, o tipo de dados será determinado na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="03321-211">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="03321-212">Número</span><span class="sxs-lookup"><span data-stu-id="03321-212">Number</span></span>
- <span data-ttu-id="03321-213">Moeda</span><span class="sxs-lookup"><span data-stu-id="03321-213">Currency</span></span>
- <span data-ttu-id="03321-214">Data</span><span class="sxs-lookup"><span data-stu-id="03321-214">Date</span></span>
- <span data-ttu-id="03321-215">Texto</span><span class="sxs-lookup"><span data-stu-id="03321-215">Text</span></span>
- <span data-ttu-id="03321-216">Booliano</span><span class="sxs-lookup"><span data-stu-id="03321-216">Boolean</span></span>

<span data-ttu-id="03321-217">Se forem encontrados dados que não correspondam ao tipo de dados adivinhados para a coluna, esses dados serão retornados como um valor **nulo** .</span><span class="sxs-lookup"><span data-stu-id="03321-217">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="03321-218">Durante uma importação, se uma coluna tem tipos de dados mistos, toda a coluna é convertida para o tipo de dados definido pela configuração **ImportMixedTypes** .</span><span class="sxs-lookup"><span data-stu-id="03321-218">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

# <a name="office-2010taboffice-2010"></a>[<span data-ttu-id="03321-219">Office 2010</span><span class="sxs-lookup"><span data-stu-id="03321-219">Office 2010</span></span>](#tab/office-2010)

<span data-ttu-id="03321-220">Para o Office de 32 bits no Windows de 32 bits ou no Office de 64 bits no Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="03321-220">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="03321-221">**Engine\Engines\Excel de conectividade HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access**</span><span class="sxs-lookup"><span data-stu-id="03321-221">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="03321-222">Para o Office de 32 bits em Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="03321-222">For 32-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="03321-223">**Engine\Engines\Excel de conectividade HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access**</span><span class="sxs-lookup"><span data-stu-id="03321-223">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="03321-224">O número padrão de linhas a serem verificadas é **8** (oito).</span><span class="sxs-lookup"><span data-stu-id="03321-224">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="03321-225">Quando você define o valor de **TypeGuessRows** para **0** (zero), o driver do Excel verifica as primeiras 16.384 linhas para o tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="03321-225">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="03321-226">Se você deseja verificar mais de 16.384 linhas, defina **TypeGuessRows** como um valor que se baseia no intervalo desejado.</span><span class="sxs-lookup"><span data-stu-id="03321-226">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="03321-227">Para verificar todas as linhas, defina **TypeGuessRows** como 1.048.576 (o número máximo de linhas permitido no Excel).</span><span class="sxs-lookup"><span data-stu-id="03321-227">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="03321-228">O tipo de dados é determinado pelo número máximo de tipos de dados que é encontrado.</span><span class="sxs-lookup"><span data-stu-id="03321-228">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="03321-229">Se houver um empate, o tipo de dados será determinado na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="03321-229">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="03321-230">Número</span><span class="sxs-lookup"><span data-stu-id="03321-230">Number</span></span>
- <span data-ttu-id="03321-231">Moeda</span><span class="sxs-lookup"><span data-stu-id="03321-231">Currency</span></span>
- <span data-ttu-id="03321-232">Data</span><span class="sxs-lookup"><span data-stu-id="03321-232">Date</span></span>
- <span data-ttu-id="03321-233">Texto</span><span class="sxs-lookup"><span data-stu-id="03321-233">Text</span></span>
- <span data-ttu-id="03321-234">Booliano</span><span class="sxs-lookup"><span data-stu-id="03321-234">Boolean</span></span>

<span data-ttu-id="03321-235">Se forem encontrados dados que não correspondam ao tipo de dados adivinhados para a coluna, esses dados serão retornados como um valor **nulo** .</span><span class="sxs-lookup"><span data-stu-id="03321-235">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="03321-236">Durante uma importação, se uma coluna tem tipos de dados mistos, toda a coluna é convertida para o tipo de dados definido pela configuração **ImportMixedTypes** .</span><span class="sxs-lookup"><span data-stu-id="03321-236">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

---
> [!NOTE]
> <span data-ttu-id="03321-237">[!OBSERVAçãO] Ao alterar as configurações do Registro do Windows, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="03321-237">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="03321-238">Confira também</span><span class="sxs-lookup"><span data-stu-id="03321-238">See also</span></span>

- [<span data-ttu-id="03321-239">Usando a configuração TypeGuessRows para o driver do Excel</span><span class="sxs-lookup"><span data-stu-id="03321-239">Using the TypeGuessRows setting for Excel Driver</span></span>](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)
