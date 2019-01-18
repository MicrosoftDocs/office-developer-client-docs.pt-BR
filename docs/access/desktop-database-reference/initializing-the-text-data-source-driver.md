---
title: Inicializando o driver de fonte de dados de texto
TOCTitle: Initializing the Text Data Source driver
ms:assetid: cba0864e-5f94-bf43-4708-b1981e3acaff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834391(v=office.15)
ms:contentKeyID: 48547718
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032166
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2e76cc7d6b5254f2347e2264b0588ee1df643d05
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709135"
---
# <a name="initializing-the-text-data-source-driver"></a><span data-ttu-id="e180b-102">Inicializando o driver de fonte de dados de texto</span><span class="sxs-lookup"><span data-stu-id="e180b-102">Initializing the Text Data Source driver</span></span>

<span data-ttu-id="e180b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="e180b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e180b-104">O mesmo driver de banco de dados é usado para ambas as fontes de dados de texto e para fontes de dados HTML.</span><span class="sxs-lookup"><span data-stu-id="e180b-104">The same database driver is used for both text data sources and for HTML data sources.</span></span>

<span data-ttu-id="e180b-105">Quando você instala o driver de banco de dados da fonte de dados de texto, o programa de instalação grava um conjunto de valores padrão para o registro do Microsoft Windows nas subchaves mecanismos e ISAM Formats.</span><span class="sxs-lookup"><span data-stu-id="e180b-105">When you install the Text Data Source database driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="e180b-106">Você não deve modificar essas configurações diretamente; use o programa de instalação de seu aplicativo para adicionar, remover ou alterar essas configurações.</span><span class="sxs-lookup"><span data-stu-id="e180b-106">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="e180b-107">As seções a seguir descrevem a inicialização e as configurações do ISAM Format no driver de banco de dados da fonte de dados de texto.</span><span class="sxs-lookup"><span data-stu-id="e180b-107">The following sections describe initialization and ISAM Format settings for the Text Data Source database driver.</span></span>

## <a name="text-data-source-initialization-settings"></a><span data-ttu-id="e180b-108">Configurações de inicialização de fonte de dados de texto</span><span class="sxs-lookup"><span data-stu-id="e180b-108">Text data source initialization settings</span></span>

<span data-ttu-id="e180b-109">O **mecanismo de conectividade do Access\\ISAM Formats\\pasta texto** inclui configurações de inicialização para o driver Acetxt.dll, usadas para acesso externo para arquivos de dados de texto.</span><span class="sxs-lookup"><span data-stu-id="e180b-109">The **Access Connectivity Engine\\ISAM Formats\\Text folder** includes initialization settings for the Acetxt.dll driver, used for external access to text data files.</span></span> <span data-ttu-id="e180b-110">As configurações normais das entradas nessa pasta são mostradas no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="e180b-110">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ ACETXT.DLL 
    
    MaxScanRows=25 
    
    FirstRowHasNames=True 
    
    CharacterSet= ANSI 
    
    Format=CSVDelimited 
    
    Extensions= txt,csv,tab,asc 
    
    ExportCurrencySymbols=Yes
```

<br/>

<span data-ttu-id="e180b-111">O mecanismo de banco de dados do Microsoft Access usa as entradas da pasta Text da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e180b-111">The Microsoft Access database engine uses the Text folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e180b-112">Entrada</span><span class="sxs-lookup"><span data-stu-id="e180b-112">Entry</span></span></p></th>
<th><p><span data-ttu-id="e180b-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="e180b-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e180b-114">Win32</span><span class="sxs-lookup"><span data-stu-id="e180b-114">win32</span></span></p></td>
<td><p><span data-ttu-id="e180b-p103">A localização do arquivo Acetxt.dll. O caminho completo é determinado no momento da instalação. Os valores são do tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="e180b-p103">The location of Acetxt.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-118">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="e180b-118">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="e180b-p104">O número de linhas a serem verificadas ao determinar os tipos de coluna. Se for 0, o arquivo inteiro será pesquisado. O padrão é 25. Os valores são do tipo REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="e180b-p104">The number of rows to be scanned when guessing the column types. If set to 0, the entire file will be searched. The default is 25. Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-123">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="e180b-123">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="e180b-p105">Um valor binário que indica se a primeira linha da tabela contém nomes de coluna. Um valor 0 indica que, durante a importação, os nomes de coluna serão extraídos da primeira linha.</span><span class="sxs-lookup"><span data-stu-id="e180b-p105">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-126">CharacterSet</span><span class="sxs-lookup"><span data-stu-id="e180b-126">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="e180b-p106">Um indicador de como as páginas de texto são armazenadas. As configurações possíveis são:</span><span class="sxs-lookup"><span data-stu-id="e180b-p106">An indicator of how text pages are stored. Possible settings are:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="e180b-p107">ANSI — a página de código ANSI do computador. São feitas as conversões AnsiToUnicode e UnicodeToAnsi.</span><span class="sxs-lookup"><span data-stu-id="e180b-p107">ANSI — The ANSI code page of the machine. AnsiToUnicode and UnicodeToAnsi conversions done.</span></span></p></li>
<li><p><span data-ttu-id="e180b-p108">OEM — a página de código OEM do computador. São feitas as conversões OemToUnicode e UnicodeToOem.</span><span class="sxs-lookup"><span data-stu-id="e180b-p108">OEM — The OEM code page of the machine. OemToUnicode and UnicodeToOem conversions done.</span></span></p></li>
<li><p><span data-ttu-id="e180b-133">Unicode — não são feitas conversões de página de código.</span><span class="sxs-lookup"><span data-stu-id="e180b-133">Unicode — codepage conversions not done.</span></span></p></li>
<li><p><span data-ttu-id="e180b-134">&lt;número decimal&gt; — o número de página de código de um conjunto de caracteres específica.</span><span class="sxs-lookup"><span data-stu-id="e180b-134">&lt;decimal number&gt; — The code page number of a specific character set.</span></span> <span data-ttu-id="e180b-135">Conversões de e para Unicode serão feitos.</span><span class="sxs-lookup"><span data-stu-id="e180b-135">Conversions to and from Unicode will be done.</span></span></p></li>
</ul>
<p></p>
<p><span data-ttu-id="e180b-p110">O padrão é ANSI. Os valores são do tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="e180b-p110">The default is ANSI. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-138">Format</span><span class="sxs-lookup"><span data-stu-id="e180b-138">Format</span></span></p></td>
<td><p><span data-ttu-id="e180b-139">Pode ser qualquer um dos seguintes: TabDelimited, CSVDelimited, delimitado (&lt;caractere único&gt;).</span><span class="sxs-lookup"><span data-stu-id="e180b-139">Can be any of the following: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;).</span></span> <span data-ttu-id="e180b-140">O delimitador caractere único no formato delimitado pode ser qualquer caractere único, exceto aspas duplas (&quot;).</span><span class="sxs-lookup"><span data-stu-id="e180b-140">The single-character delimiter in the Delimited format can be any single character except a double quotation mark (&quot;).</span></span> <span data-ttu-id="e180b-141">O padrão é CSVDelimited.</span><span class="sxs-lookup"><span data-stu-id="e180b-141">The default is CSVDelimited.</span></span> <span data-ttu-id="e180b-142">Os valores são do tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="e180b-142">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-143">Extensions</span><span class="sxs-lookup"><span data-stu-id="e180b-143">Extensions</span></span></p></td>
<td><p><span data-ttu-id="e180b-p112">A extensão de qualquer arquivo a ser pesquisado ao procurar dados baseados em texto. O padrão é txt, csv, tab, asc. Os valores são do tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="e180b-p112">The extension of any files to be browsed when looking for text-based data. The default is txt, csv, tab, asc. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-147">ExportCurrencySymbols</span><span class="sxs-lookup"><span data-stu-id="e180b-147">ExportCurrencySymbols</span></span></p></td>
<td><p><span data-ttu-id="e180b-p113">Um valor binário que indica se o símbolo de moeda apropriado é incluído quando os campos de moeda são exportados. Um valor 01 indica que o símbolo é incluído. Um valor 00 indica que apenas os dados numéricos são exportados. O valor padrão é 01. Os valores são do tipo REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="e180b-p113">A binary value that indicates whether the appropriate currency symbol is included when currency fields are exported. A value of 01 indicates that the symbol is included. A value of 00 indicates that only the numeric data is exported. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="text-data-source-isam-formats"></a><span data-ttu-id="e180b-153">ISAM formats da fonte de dados texto</span><span class="sxs-lookup"><span data-stu-id="e180b-153">Text data source ISAM formats</span></span>

<span data-ttu-id="e180b-154">O **mecanismo de conectividade do Access\\ISAM Formats\\texto** pasta contém as entradas a seguir.</span><span class="sxs-lookup"><span data-stu-id="e180b-154">The **Access Connectivity Engine\\ISAM Formats\\Text** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e180b-155">Nome da entrada</span><span class="sxs-lookup"><span data-stu-id="e180b-155">Entry name</span></span></p></th>
<th><p><span data-ttu-id="e180b-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="e180b-156">Type</span></span></p></th>
<th><p><span data-ttu-id="e180b-157">Valor</span><span class="sxs-lookup"><span data-stu-id="e180b-157">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e180b-158">Engine</span><span class="sxs-lookup"><span data-stu-id="e180b-158">Engine</span></span></p></td>
<td><p><span data-ttu-id="e180b-159">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e180b-159">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e180b-160">Texto</span><span class="sxs-lookup"><span data-stu-id="e180b-160">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-161">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="e180b-161">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="e180b-162">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e180b-162">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e180b-163">Arquivos de texto (\*.txt; \*.csv; \*.tab; \*.asc)</span><span class="sxs-lookup"><span data-stu-id="e180b-163">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-164">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="e180b-164">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="e180b-165">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e180b-165">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e180b-166">Arquivos de texto (\*.txt; \*.csv; \*.tab; \*.asc)</span><span class="sxs-lookup"><span data-stu-id="e180b-166">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-167">CanLink</span><span class="sxs-lookup"><span data-stu-id="e180b-167">CanLink</span></span></p></td>
<td><p><span data-ttu-id="e180b-168">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="e180b-168">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="e180b-169">01</span><span class="sxs-lookup"><span data-stu-id="e180b-169">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-170">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="e180b-170">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="e180b-171">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="e180b-171">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="e180b-172">01</span><span class="sxs-lookup"><span data-stu-id="e180b-172">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-173">IsamType</span><span class="sxs-lookup"><span data-stu-id="e180b-173">IsamType</span></span></p></td>
<td><p><span data-ttu-id="e180b-174">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e180b-174">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="e180b-175">2</span><span class="sxs-lookup"><span data-stu-id="e180b-175">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-176">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="e180b-176">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="e180b-177">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="e180b-177">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="e180b-178">00</span><span class="sxs-lookup"><span data-stu-id="e180b-178">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-179">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="e180b-179">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="e180b-180">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="e180b-180">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="e180b-181">00</span><span class="sxs-lookup"><span data-stu-id="e180b-181">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-182">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="e180b-182">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="e180b-183">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e180b-183">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e180b-p114">Importar dados do arquivo externo para o banco de dados atual. Alterar dados no banco de dados atual não os alterará no arquivo externo.</span><span class="sxs-lookup"><span data-stu-id="e180b-p114">Import data from the external file into the current database. Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-186">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="e180b-186">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="e180b-187">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e180b-187">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e180b-p115">Criar uma tabela no banco de dados atual vinculada ao arquivo externo. Alterar dados no banco de dados atual não os alterará no arquivo externo.</span><span class="sxs-lookup"><span data-stu-id="e180b-p115">Create a table in the current database that is linked to the external file. Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-190">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="e180b-190">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="e180b-191">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e180b-191">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e180b-p116">Exportar dados do banco de dados atual para um arquivo de texto. Esse processo substituirá os dados quando exportados para um arquivo já existente.</span><span class="sxs-lookup"><span data-stu-id="e180b-p116">Export data from the current database into a text file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-194">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="e180b-194">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="e180b-195">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="e180b-195">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="e180b-196">01</span><span class="sxs-lookup"><span data-stu-id="e180b-196">01</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="e180b-197">Ao alterar as configurações do Registro do Windows, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="e180b-197">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="html-import-isam-formats"></a><span data-ttu-id="e180b-198">ISAM formats para HTML import</span><span class="sxs-lookup"><span data-stu-id="e180b-198">HTML import ISAM formats</span></span>

<span data-ttu-id="e180b-199">O **mecanismo de conectividade do Access\\ISAM Formats\\HTML Import** pasta contém as entradas a seguir.</span><span class="sxs-lookup"><span data-stu-id="e180b-199">The **Access Connectivity Engine\\ISAM Formats\\HTML Import** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e180b-200">Nome da entrada</span><span class="sxs-lookup"><span data-stu-id="e180b-200">Entry name</span></span></p></th>
<th><p><span data-ttu-id="e180b-201">Tipo</span><span class="sxs-lookup"><span data-stu-id="e180b-201">Type</span></span></p></th>
<th><p><span data-ttu-id="e180b-202">Valor</span><span class="sxs-lookup"><span data-stu-id="e180b-202">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e180b-203">Engine</span><span class="sxs-lookup"><span data-stu-id="e180b-203">Engine</span></span></p></td>
<td><p><span data-ttu-id="e180b-204">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e180b-204">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e180b-205">Texto</span><span class="sxs-lookup"><span data-stu-id="e180b-205">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-206">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="e180b-206">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="e180b-207">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e180b-207">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e180b-208">Arquivos HTML (*. HT*)</span><span class="sxs-lookup"><span data-stu-id="e180b-208">HTML Files (*.ht*)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-209">CanLink</span><span class="sxs-lookup"><span data-stu-id="e180b-209">CanLink</span></span></p></td>
<td><p><span data-ttu-id="e180b-210">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="e180b-210">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="e180b-211">01</span><span class="sxs-lookup"><span data-stu-id="e180b-211">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-212">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="e180b-212">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="e180b-213">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="e180b-213">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="e180b-214">00</span><span class="sxs-lookup"><span data-stu-id="e180b-214">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-215">IsamType</span><span class="sxs-lookup"><span data-stu-id="e180b-215">IsamType</span></span></p></td>
<td><p><span data-ttu-id="e180b-216">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e180b-216">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="e180b-217">2</span><span class="sxs-lookup"><span data-stu-id="e180b-217">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-218">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="e180b-218">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="e180b-219">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="e180b-219">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="e180b-220">00</span><span class="sxs-lookup"><span data-stu-id="e180b-220">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-221">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="e180b-221">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="e180b-222">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="e180b-222">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="e180b-223">00</span><span class="sxs-lookup"><span data-stu-id="e180b-223">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-224">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="e180b-224">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="e180b-225">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e180b-225">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e180b-p117">Importar dados do arquivo externo para o banco de dados atual. Alterar dados no banco de dados atual não os alterará no arquivo externo.</span><span class="sxs-lookup"><span data-stu-id="e180b-p117">Import data from the external file into the current database. Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-228">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="e180b-228">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="e180b-229">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e180b-229">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e180b-p118">Criar uma tabela no banco de dados atual vinculada ao arquivo externo. Alterar dados no banco de dados atual não os alterará no arquivo externo.</span><span class="sxs-lookup"><span data-stu-id="e180b-p118">Create a table in the current database that is linked to the external file. Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-232">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="e180b-232">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="e180b-233">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="e180b-233">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="e180b-234">01</span><span class="sxs-lookup"><span data-stu-id="e180b-234">01</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e180b-235">Ao alterar as configurações do Registro do Windows, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="e180b-235">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="html-export-isam-formats"></a><span data-ttu-id="e180b-236">ISAM formats do HTML export</span><span class="sxs-lookup"><span data-stu-id="e180b-236">HTML export ISAM formats</span></span>

<span data-ttu-id="e180b-237">O **mecanismo de conectividade do Access\\ISAM Formats\\HTML Export** pasta contém as entradas a seguir.</span><span class="sxs-lookup"><span data-stu-id="e180b-237">The **Access Connectivity Engine\\ISAM Formats\\HTML Export** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e180b-238">Nome da entrada</span><span class="sxs-lookup"><span data-stu-id="e180b-238">Entry name</span></span></p></th>
<th><p><span data-ttu-id="e180b-239">Tipo</span><span class="sxs-lookup"><span data-stu-id="e180b-239">Type</span></span></p></th>
<th><p><span data-ttu-id="e180b-240">Valor</span><span class="sxs-lookup"><span data-stu-id="e180b-240">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e180b-241">Engine</span><span class="sxs-lookup"><span data-stu-id="e180b-241">Engine</span></span></p></td>
<td><p><span data-ttu-id="e180b-242">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e180b-242">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e180b-243">Texto</span><span class="sxs-lookup"><span data-stu-id="e180b-243">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-244">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="e180b-244">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="e180b-245">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e180b-245">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e180b-246">Arquivos HTML (\*.htm)</span><span class="sxs-lookup"><span data-stu-id="e180b-246">HTML Files (\*.htm)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-247">CanLink</span><span class="sxs-lookup"><span data-stu-id="e180b-247">CanLink</span></span></p></td>
<td><p><span data-ttu-id="e180b-248">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="e180b-248">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="e180b-249">00</span><span class="sxs-lookup"><span data-stu-id="e180b-249">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-250">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="e180b-250">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="e180b-251">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="e180b-251">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="e180b-252">01</span><span class="sxs-lookup"><span data-stu-id="e180b-252">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-253">IsamType</span><span class="sxs-lookup"><span data-stu-id="e180b-253">IsamType</span></span></p></td>
<td><p><span data-ttu-id="e180b-254">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e180b-254">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="e180b-255">2</span><span class="sxs-lookup"><span data-stu-id="e180b-255">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-256">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="e180b-256">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="e180b-257">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="e180b-257">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="e180b-258">00</span><span class="sxs-lookup"><span data-stu-id="e180b-258">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-259">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="e180b-259">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="e180b-260">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="e180b-260">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="e180b-261">00</span><span class="sxs-lookup"><span data-stu-id="e180b-261">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-262">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="e180b-262">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="e180b-263">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e180b-263">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e180b-p119">Exportar dados do banco de dados atual para um arquivo de texto. Esse processo substituirá os dados quando exportados para um arquivo já existente.</span><span class="sxs-lookup"><span data-stu-id="e180b-p119">Export data from the current database into a text file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-266">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="e180b-266">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="e180b-267">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="e180b-267">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="e180b-268">01</span><span class="sxs-lookup"><span data-stu-id="e180b-268">01</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e180b-269">Ao alterar as configurações do Registro do Windows, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="e180b-269">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a><span data-ttu-id="e180b-270">Personalizando o arquivo Schema ini para dados HTML e texto</span><span class="sxs-lookup"><span data-stu-id="e180b-270">Customizing the Schema.ini file for text and HTML data</span></span>

<span data-ttu-id="e180b-p120">Para ler, importar ou exportar dados HTML e de texto, você precisa criar um arquivo Schema.ini, bem como incluir as informações ISAM do texto no arquivo .ini. O arquivo Schema.ini contém informações específicas da fonte de dados: como o arquivo de texto está formatado, como ele é lido no momento da importação e o formato de exportação padrão dos arquivos. Os exemplos a seguir mostram o layout de um arquivo de largura fixa, Filename.txt:</span><span class="sxs-lookup"><span data-stu-id="e180b-p120">To read, import, or export text and HTML data, you need to create a Schema.ini file in addition to including the Text ISAM information in the .ini file. Schema.ini contains the specifics of a data source: how the text file is formatted, how it is read at import time, and what the default export format is for files. The following examples show the layout for a fixed-width file, Filename.txt:</span></span>

```text
    [Filename.txt] 
    
    ColNameHeader=False 
    
    Format=FixedLength 
    
    FixedFormat= RaggedEdge 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    Col1=columnname Char Width 24 
    
    Col2=columnname2 Date Width 9 
    
    Col3=columnname7 Float Width 10 
    
    Col4=columnname8 Integer Width 10 
    Col5=columnname9 LongChar Width 10
```

<br/>

<span data-ttu-id="e180b-274">Da mesma maneira, o formato de um arquivo delimitado é especificado assim:</span><span class="sxs-lookup"><span data-stu-id="e180b-274">Similarly, the format for a delimited file is specified as follows:</span></span>

```text
    [Delimit.txt] 
    
    ColNameHeader=True 
    
    Format=Delimited() 
    
    MaxScanRows=0 
    
    CharacterSet=OEM 
    
    Col1=username char width 50 
    
    Col2=dateofbirth Date width 9
```

<br/>

<span data-ttu-id="e180b-275">Se estiver exportando dados para um arquivo de texto delimitado, especifique o formato desse arquivo também:</span><span class="sxs-lookup"><span data-stu-id="e180b-275">If you are exporting data into a delimited text file, specify the format for that file as well:</span></span>

```text
    [Export: My Special Export] 
    
    ColNameHeader=True 
    
    Format=TabDelimited 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    DateTimeFormat=mm.dd.yy.hh.mm.ss 
    
    CurrencySymbol=Dm 
    
    CurrencyPosFormat=0 
    
    CurrencyDigits=2 
    
    CurrencyNegFormat=0 
    
    CurrencyThousandSymbol=, 
    
    CurrencyDecimalSymbol=. 
    
    DecimalSymbol=, 
    
    NumberDigits=2 
    
    NumberLeadingZeros=0 
    
    TextDelimeter="
```

<br/>

<span data-ttu-id="e180b-p121">O exemplo My Special Export refere-se a uma opção de exportação específica; você pode determinar qualquer variação das opções de exportação no momento da conexão. Este último exemplo também corresponde ao nome da fonte de dados (DSN) que pode ser opcionalmente passado no momento da conexão. Todas as três seções de formato podem ser incluídas no arquivo .ini.</span><span class="sxs-lookup"><span data-stu-id="e180b-p121">The My Special Export example refers to a specific export option; you can specify any variation of export options at connect time. This last example also corresponds to a data source name (DSN) that can be optionally passed at connect time. All three format sections can be included in the same .ini file.</span></span>

<span data-ttu-id="e180b-279">O mecanismo de banco de dados do Microsoft Access usa as entradas do Schema.ini da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e180b-279">The Microsoft Access database engine uses the Schema.ini entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e180b-280">Entrada</span><span class="sxs-lookup"><span data-stu-id="e180b-280">Entry</span></span></p></th>
<th><p><span data-ttu-id="e180b-281">Descrição</span><span class="sxs-lookup"><span data-stu-id="e180b-281">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e180b-282">ColNameHeader</span><span class="sxs-lookup"><span data-stu-id="e180b-282">ColNameHeader</span></span></p></td>
<td><p><span data-ttu-id="e180b-283">Pode ser <strong>True</strong> (indicando que o primeiro registro dos dados especifica os nomes das colunas) ou <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="e180b-283">Can be set to either <strong>True</strong> (indicating that the first record of data specifies the column names) or <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-284">Formatar</span><span class="sxs-lookup"><span data-stu-id="e180b-284">Format</span></span></p></td>
<td><p><span data-ttu-id="e180b-285">Pode ser definido como um dos seguintes valores: TabDelimited, CSVDelimited, delimitado (&lt;caractere único&gt;), ou FixedLength.</span><span class="sxs-lookup"><span data-stu-id="e180b-285">Can be set to one of the following values: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;), or FixedLength.</span></span> <span data-ttu-id="e180b-286">O delimitador especificado para o formato de arquivo delimitado pode ser qualquer caractere único, exceto aspas duplas (&quot;).</span><span class="sxs-lookup"><span data-stu-id="e180b-286">The delimiter specified for the Delimited file format can be any single character except a double quotation mark (&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-287">FixedFormat</span><span class="sxs-lookup"><span data-stu-id="e180b-287">FixedFormat</span></span></p></td>
<td><p><span data-ttu-id="e180b-288">Usado somente quando Format é FixedLength; pode ser definido como: RaggedEdge ou TrueFixedLength.
</span><span class="sxs-lookup"><span data-stu-id="e180b-288">Only used when the Format is FixedLength, this can be set to one of the following values: RaggedEdge or TrueFixedLength.</span></span> <span data-ttu-id="e180b-289">RaggedEdge permite que as linhas terminem com um caractere de retorno de carro.</span><span class="sxs-lookup"><span data-stu-id="e180b-289">RaggedEdge allows rows to be terminated with a Carriage Return character.</span></span> <span data-ttu-id="e180b-290">TrueFixedLength exige que cada linha tenha um número exato de caracteres e qualquer caractere de retorno de carro que não estiver no limite da linha será considerado incorporado ao campo.</span><span class="sxs-lookup"><span data-stu-id="e180b-290">TrueFixedLength requires each row to be an exact number of characters, and any Carriage Return characters not at a row boundary are assumed to be embedded in a field.</span></span> <span data-ttu-id="e180b-291">Se essa configuração não estiver presente, o valor padrão será RaggedEdge.</span><span class="sxs-lookup"><span data-stu-id="e180b-291">If this setting is not present, the default value is RaggedEdge.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-292">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="e180b-292">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="e180b-p124">Indica o número de linhas a serem verificadas ao determinar os tipos de dados da coluna. Se estiver definido como 0, o arquivo inteiro será pesquisado.</span><span class="sxs-lookup"><span data-stu-id="e180b-p124">Indicates the number of rows to be scanned when guessing the column data types. If this is set to 0, the entire file is searched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-295">CharacterSet</span><span class="sxs-lookup"><span data-stu-id="e180b-295">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="e180b-296">Pode ser definido como OEM, ANSI, UNICODE ou o número decimal de uma página de código válida e indica o conjunto de caracteres do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="e180b-296">Can be set to OEM, ANSI, UNICODE, or the decimal number of a valid code page, and indicates the character set of the source file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-297">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="e180b-297">DateTimeFormat</span></span></p></td>
<td><p><span data-ttu-id="e180b-p125">Pode ser definida como uma cadeia de caracteres de formatação indicando datas e horas. Essa entrada deverá ser especificada se todos os campos de data/hora na importação/exportação forem tratados como sendo do mesmo formato. Há suporte para todos os formatos do mecanismo de banco de dados Microsoft Jet, com exceção de AM e PM. Na ausência de uma cadeia de caracteres de formatação, as opções de data e hora curtas do Painel de Controle do Windows serão usadas.</span><span class="sxs-lookup"><span data-stu-id="e180b-p125">Can be set to a format string indicating dates and times. This entry should be specified if all date/time fields in the import/export are handled with the same format. All of the Microsoft Jet database engine formats except AM and PM are supported. In the absence of a format string, the Windows Control Panel short date picture and time options are used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-302">CurrencySymbol</span><span class="sxs-lookup"><span data-stu-id="e180b-302">CurrencySymbol</span></span></p></td>
<td><p><span data-ttu-id="e180b-p126">Indica o símbolo de moeda a ser usado nos valores de moeda do arquivo de texto. Os exemplos incluem o símbolo do dólar ($) e Dm. Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</span><span class="sxs-lookup"><span data-stu-id="e180b-p126">Indicates the currency symbol to be used for currency values in the text file. Examples include the dollar sign ($) and Dm. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-306">CurrencyPosFormat</span><span class="sxs-lookup"><span data-stu-id="e180b-306">CurrencyPosFormat</span></span></p></td>
<td><p><span data-ttu-id="e180b-307">Pode ser definido como qualquer um dos seguintes valores: prefixo de símbolo de moeda com o sufixo de símbolo de moeda sem separação ($1) sem separação (1$) prefixo de símbolo de moeda com o sufixo de símbolo de moeda de separação ($ 1) de um caractere com separação de um caractere (1 $) se essa entrada não estiver presente, o valor padrão no painel de controle do Windows é usado.</span><span class="sxs-lookup"><span data-stu-id="e180b-307">Can be set to any of the following values: Currency symbol prefix with no separation ($1) Currency symbol suffix with no separation (1$) Currency symbol prefix with one character separation ($ 1) Currency symbol suffix with one character separation (1 $) If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-308">CurrencyDigits</span><span class="sxs-lookup"><span data-stu-id="e180b-308">CurrencyDigits</span></span></p></td>
<td><p><span data-ttu-id="e180b-p127">Especifica o número de dígitos usados na parte fracional do valor da moeda. Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</span><span class="sxs-lookup"><span data-stu-id="e180b-p127">Specifies the number of digits used for the fractional part of a currency amount. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-311">CurrencyNegFormat</span><span class="sxs-lookup"><span data-stu-id="e180b-311">CurrencyNegFormat</span></span></p></td>
<td><p><span data-ttu-id="e180b-312">Pode ser um dos seguintes valores: ($1) – $1 $– 1 $1 – (1$) – 1$ $ 1 a US $ 1 – – 1 $ – $ 1 1 $– $ 1 – $ – 1 1 – $ ($ 1) (1 $) cifrão é mostrado para os fins deste exemplo, mas deveria ser substituído pelo valor CurrencySymbol apropriado no programa real.</span><span class="sxs-lookup"><span data-stu-id="e180b-312">Can be one of the following values: ($1) –$1 $–1 $1– (1$) –1$ 1–$ 1$– –1 $ –$ 1 1 $– $ 1– $ –1 1– $ ($ 1) (1 $) The dollar sign is shown for purposes of this example, but it should be replaced with the appropriate CurrencySymbol value in the actual program.</span></span> <span data-ttu-id="e180b-313">Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</span><span class="sxs-lookup"><span data-stu-id="e180b-313">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-314">CurrencyThousandSymbol</span><span class="sxs-lookup"><span data-stu-id="e180b-314">CurrencyThousandSymbol</span></span></p></td>
<td><p><span data-ttu-id="e180b-p129">Indica o símbolo de um caractere a ser usado para separar os milhares dos valores de moeda no arquivo de texto. Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</span><span class="sxs-lookup"><span data-stu-id="e180b-p129">Indicates the single-character symbol to be used for separating currency values by thousands in the text file. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-317">CurrencyDecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="e180b-317">CurrencyDecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="e180b-p130">Pode ser definido como qualquer caractere usado para separar a parte fracional do valor da moeda. Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</span><span class="sxs-lookup"><span data-stu-id="e180b-p130">Can be set to any single character that is used to separate the whole from the fractional part of a currency amount. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-320">DecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="e180b-320">DecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="e180b-p131">Pode ser definido como qualquer caractere usado para separar o inteiro da parte fracional de um número. Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</span><span class="sxs-lookup"><span data-stu-id="e180b-p131">Can be set to any single character that is used to separate the integer from the fractional part of a number. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-323">NumberDigits</span><span class="sxs-lookup"><span data-stu-id="e180b-323">NumberDigits</span></span></p></td>
<td><p><span data-ttu-id="e180b-p132">Indica o número de dígitos decimais usados na parte fracional de um número. Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</span><span class="sxs-lookup"><span data-stu-id="e180b-p132">Indicates the number of decimal digits in the fractional portion of a number. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-326">NumberLeadingZeros</span><span class="sxs-lookup"><span data-stu-id="e180b-326">NumberLeadingZeros</span></span></p></td>
<td><p><span data-ttu-id="e180b-327">Especifica se um valor decimal inferior a 1 e superior a –1 deve conter zeros à esquerda; esse valor pode ser False (sem zeros à esquerda) ou True.</span><span class="sxs-lookup"><span data-stu-id="e180b-327">Specifies whether a decimal value less than 1 and greater than –1 should contain leading zeros; this value can either be False (no leading zeros) or True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e180b-328">Col1, Col2, …</span><span class="sxs-lookup"><span data-stu-id="e180b-328">Col1, Col2, …</span></span></p></td>
<td><p><span data-ttu-id="e180b-329">Lista as colunas no arquivo de texto a ser lido.</span><span class="sxs-lookup"><span data-stu-id="e180b-329">Lists the columns in the text file to be read.</span></span> <span data-ttu-id="e180b-330">O formato dessa entrada deve ser: <em>Coln</em>=<em>columnName</em> tipo [largura <em> #</em>] <em>columnName</em>: nomes de colunas com espaços incorporados devem estar entre aspas.</span><span class="sxs-lookup"><span data-stu-id="e180b-330">The format of this entry should be: <em>Coln</em>=<em>columnName</em> type [Width <em>#</em>] <em>columnName</em>: Column names with embedded spaces should be enclosed in quotation marks.</span></span> <span data-ttu-id="e180b-331"><em>tipo</em>: pode ser Bit, Byte, Short, Long, Decimal, moeda, único, duplo, data/hora.</span><span class="sxs-lookup"><span data-stu-id="e180b-331"><em>type</em>: Can be Bit, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime.</span></span> <span data-ttu-id="e180b-332">Binário, OLE, texto ou Memorando.</span><span class="sxs-lookup"><span data-stu-id="e180b-332">Binary, OLE, Text, or Memo.</span></span> <span data-ttu-id="e180b-333">Além disso, os seguintes tipos de Driver de texto ODBC são suportados: Char (mesmo que Text) Float (mesmo que Double) Integer (mesmo que Short) LongChar (mesmo que Memo) Date <em>formato de data</em> no caso de um marcador de formato adicional [Attribute Hyperlink] pode ser um tipo de memorando usado para especificar as colunas que devem ser URLs ativas no Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="e180b-333">In addition, the following ODBC Text Driver types are supported: Char (same as Text) Float (same as Double) Integer (same as Short) LongChar (same as Memo) Date <em>date format</em> In the case of a Memo type an additional format marker [Attribute Hyperlink] can be used to specify columns that should be active URLs in Microsoft Access.</span></span> <span data-ttu-id="e180b-334">No caso de um tipo Decimal, marcadores de formato adicionais [Scale #] Precision #] devem ser usados.</span><span class="sxs-lookup"><span data-stu-id="e180b-334">In the case of a Decimal type the additional format markers [Scale #] Precision #] should be used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e180b-335">TextDelimiter</span><span class="sxs-lookup"><span data-stu-id="e180b-335">TextDelimiter</span></span></p></td>
<td><p><span data-ttu-id="e180b-336">Pode ser qualquer caractere usado para delimitar cadeias de caracteres que contenham qualquer um dos outros caracteres especiais.
</span><span class="sxs-lookup"><span data-stu-id="e180b-336">Can be set to any single character that is used to delimit strings that contain any of the other special characters.</span></span> <span data-ttu-id="e180b-337">Por exemplo</span><span class="sxs-lookup"><span data-stu-id="e180b-337">E.g.</span></span> <span data-ttu-id="e180b-338">&quot;ABC&quot;,&quot;xyz, pqr&quot;,&quot;hij&quot; se essa entrada não estiver presente o delimitador padrão será as aspas duplas.</span><span class="sxs-lookup"><span data-stu-id="e180b-338">&quot;abc&quot;,&quot;xyz,pqr&quot;,&quot;hij&quot; If this entry is not present the default delimiter is a double quote.</span></span> <span data-ttu-id="e180b-339">Se essa entrada é a cadeia de caracteres &quot;nenhum&quot; e nenhum caractere será tratado como delimitadores.</span><span class="sxs-lookup"><span data-stu-id="e180b-339">If this entry is the string &quot;none&quot; then no characters will be treated as delimiters.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e180b-340">[!OBSERVAçãO] Ao alterar as configurações do arquivo Schema.ini, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="e180b-340">When you change Schema.ini file settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>


