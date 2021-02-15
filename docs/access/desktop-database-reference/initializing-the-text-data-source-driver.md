---
title: Inicializando o driver de Fonte de Dados de Texto
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291418"
---
# <a name="initializing-the-text-data-source-driver"></a><span data-ttu-id="78cbf-102">Inicializando o driver de Fonte de Dados de Texto</span><span class="sxs-lookup"><span data-stu-id="78cbf-102">Initializing the Text Data Source driver</span></span>

<span data-ttu-id="78cbf-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="78cbf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="78cbf-104">O mesmo driver de banco de dados é usado para fontes de dados de texto e para fontes de dados HTML.</span><span class="sxs-lookup"><span data-stu-id="78cbf-104">The same database driver is used for both text data sources and for HTML data sources.</span></span>

<span data-ttu-id="78cbf-105">Quando você instala o driver de banco de dados de Fonte de Dados de Texto, o programa de Instalação grava um conjunto de valores padrão no Registro do Microsoft Windows nas sub-chaves Engines e ISAM Formats.</span><span class="sxs-lookup"><span data-stu-id="78cbf-105">When you install the Text Data Source database driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="78cbf-106">Você não deve modificar essas configurações diretamente; use o programa de instalação de seu aplicativo para adicionar, remover ou alterar essas configurações.</span><span class="sxs-lookup"><span data-stu-id="78cbf-106">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="78cbf-107">As seções a seguir descrevem a inicialização e as configurações do ISAM Format no driver de banco de dados da fonte de dados de texto.</span><span class="sxs-lookup"><span data-stu-id="78cbf-107">The following sections describe initialization and ISAM Format settings for the Text Data Source database driver.</span></span>

## <a name="text-data-source-initialization-settings"></a><span data-ttu-id="78cbf-108">Configurações de inicialização da fonte de dados de texto</span><span class="sxs-lookup"><span data-stu-id="78cbf-108">Text data source initialization settings</span></span>

<span data-ttu-id="78cbf-109">A **pasta Texto \\ isam \\ formats** do mecanismo de conectividade de acesso inclui configurações de inicialização para o driver Acetxt.dll, usado para acesso externo a arquivos de dados de texto.</span><span class="sxs-lookup"><span data-stu-id="78cbf-109">The **Access Connectivity Engine\\ISAM Formats\\Text folder** includes initialization settings for the Acetxt.dll driver, used for external access to text data files.</span></span> <span data-ttu-id="78cbf-110">As configurações normais das entradas nessa pasta são mostradas no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="78cbf-110">Typical settings for the entries in this folder are shown in the following example.</span></span>

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

<span data-ttu-id="78cbf-111">O mecanismo de banco de dados do Microsoft Access usa as entradas da pasta Text da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="78cbf-111">The Microsoft Access database engine uses the Text folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="78cbf-112">Entrada</span><span class="sxs-lookup"><span data-stu-id="78cbf-112">Entry</span></span></p></th>
<th><p><span data-ttu-id="78cbf-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="78cbf-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-114">win32</span><span class="sxs-lookup"><span data-stu-id="78cbf-114">win32</span></span></p></td>
<td><p><span data-ttu-id="78cbf-p103">A localização do arquivo Acetxt.dll. O caminho completo é determinado no momento da instalação. Os valores são do tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p103">The location of Acetxt.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-118">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="78cbf-118">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="78cbf-p104">O número de linhas a serem verificadas ao determinar os tipos de coluna. Se for 0, o arquivo inteiro será pesquisado. O padrão é 25. Os valores são do tipo REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p104">The number of rows to be scanned when guessing the column types. If set to 0, the entire file will be searched. The default is 25. Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-123">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="78cbf-123">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="78cbf-p105">Um valor binário que indica se a primeira linha da tabela contém nomes de coluna. Um valor 0 indica que, durante a importação, os nomes de coluna serão extraídos da primeira linha.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p105">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-126">CharacterSet</span><span class="sxs-lookup"><span data-stu-id="78cbf-126">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="78cbf-127">Um indicador de como as páginas de texto são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="78cbf-127">An indicator of how text pages are stored.</span></span> <span data-ttu-id="78cbf-128">As configurações possíveis são:</span><span class="sxs-lookup"><span data-stu-id="78cbf-128">Possible settings are:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="78cbf-129">ANSI — a página de código ANSI do computador.</span><span class="sxs-lookup"><span data-stu-id="78cbf-129">ANSI — The ANSI code page of the machine.</span></span> <span data-ttu-id="78cbf-130">São feitas as conversões AnsiToUnicode e UnicodeToAnsi.</span><span class="sxs-lookup"><span data-stu-id="78cbf-130">AnsiToUnicode and UnicodeToAnsi conversions done.</span></span></p></li>
<li><p><span data-ttu-id="78cbf-131">OEM — a página de código OEM do computador.</span><span class="sxs-lookup"><span data-stu-id="78cbf-131">OEM — The OEM code page of the machine.</span></span> <span data-ttu-id="78cbf-132">São feitas as conversões OemToUnicode e UnicodeToOem.</span><span class="sxs-lookup"><span data-stu-id="78cbf-132">OemToUnicode and UnicodeToOem conversions done.</span></span></p></li>
<li><p><span data-ttu-id="78cbf-133">Unicode — não são feitas conversões de página de código.</span><span class="sxs-lookup"><span data-stu-id="78cbf-133">Unicode — codepage conversions not done.</span></span></p></li>
<li><p><span data-ttu-id="78cbf-134">&lt;número decimal &gt; — o número da página de código de um conjunto de caracteres específico.</span><span class="sxs-lookup"><span data-stu-id="78cbf-134">&lt;decimal number&gt; — The code page number of a specific character set.</span></span> <span data-ttu-id="78cbf-135">As conversões de e para Unicode serão feitas.</span><span class="sxs-lookup"><span data-stu-id="78cbf-135">Conversions to and from Unicode will be done.</span></span></p></li>
</ul>
<p></p>
<p><span data-ttu-id="78cbf-136">O padrão é ANSI.</span><span class="sxs-lookup"><span data-stu-id="78cbf-136">The default is ANSI.</span></span> <span data-ttu-id="78cbf-137">Os valores são do tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="78cbf-137">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-138">Formatar</span><span class="sxs-lookup"><span data-stu-id="78cbf-138">Format</span></span></p></td>
<td><p><span data-ttu-id="78cbf-139">Pode ser qualquer um dos seguintes: TabDelimited, CSVDelimited, Delimited ( &lt; caractere único &gt; ).</span><span class="sxs-lookup"><span data-stu-id="78cbf-139">Can be any of the following: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;).</span></span> <span data-ttu-id="78cbf-140">O delimitador de caractere único no formato Delimitado pode ser qualquer caractere, exceto aspas duplas ( &quot; ).</span><span class="sxs-lookup"><span data-stu-id="78cbf-140">The single-character delimiter in the Delimited format can be any single character except a double quotation mark (&quot;).</span></span> <span data-ttu-id="78cbf-141">O padrão é CSVDelimited.</span><span class="sxs-lookup"><span data-stu-id="78cbf-141">The default is CSVDelimited.</span></span> <span data-ttu-id="78cbf-142">Os valores são do tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="78cbf-142">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-143">Extensões</span><span class="sxs-lookup"><span data-stu-id="78cbf-143">Extensions</span></span></p></td>
<td><p><span data-ttu-id="78cbf-p112">A extensão de qualquer arquivo a ser pesquisado ao procurar dados baseados em texto. O padrão é txt, csv, tab, asc. Os valores são do tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p112">The extension of any files to be browsed when looking for text-based data. The default is txt, csv, tab, asc. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-147">ExportCurrencySymbols</span><span class="sxs-lookup"><span data-stu-id="78cbf-147">ExportCurrencySymbols</span></span></p></td>
<td><p><span data-ttu-id="78cbf-p113">Um valor binário que indica se o símbolo de moeda apropriado é incluído quando os campos de moeda são exportados. Um valor 01 indica que o símbolo é incluído. Um valor 00 indica que apenas os dados numéricos são exportados. O valor padrão é 01. Os valores são do tipo REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p113">A binary value that indicates whether the appropriate currency symbol is included when currency fields are exported. A value of 01 indicates that the symbol is included. A value of 00 indicates that only the numeric data is exported. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="text-data-source-isam-formats"></a><span data-ttu-id="78cbf-153">Formatos ISAM de fonte de dados de texto</span><span class="sxs-lookup"><span data-stu-id="78cbf-153">Text data source ISAM formats</span></span>

<span data-ttu-id="78cbf-154">A **pasta Texto de \\ Formatos ISAM do \\** Mecanismo de Conectividade do Access contém as entradas a seguir.</span><span class="sxs-lookup"><span data-stu-id="78cbf-154">The **Access Connectivity Engine\\ISAM Formats\\Text** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="78cbf-155">Nome da entrada</span><span class="sxs-lookup"><span data-stu-id="78cbf-155">Entry name</span></span></p></th>
<th><p><span data-ttu-id="78cbf-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="78cbf-156">Type</span></span></p></th>
<th><p><span data-ttu-id="78cbf-157">Valor</span><span class="sxs-lookup"><span data-stu-id="78cbf-157">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-158">Mecanismo</span><span class="sxs-lookup"><span data-stu-id="78cbf-158">Engine</span></span></p></td>
<td><p><span data-ttu-id="78cbf-159">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="78cbf-159">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="78cbf-160">Texto</span><span class="sxs-lookup"><span data-stu-id="78cbf-160">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-161">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="78cbf-161">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="78cbf-162">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="78cbf-162">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="78cbf-163">Arquivos de texto (\*.txt; \*.csv; \*.tab; \*.asc)</span><span class="sxs-lookup"><span data-stu-id="78cbf-163">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-164">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="78cbf-164">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="78cbf-165">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="78cbf-165">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="78cbf-166">Arquivos de texto (\*.txt; \*.csv; \*.tab; \*.asc)</span><span class="sxs-lookup"><span data-stu-id="78cbf-166">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-167">CanLink</span><span class="sxs-lookup"><span data-stu-id="78cbf-167">CanLink</span></span></p></td>
<td><p><span data-ttu-id="78cbf-168">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="78cbf-168">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="78cbf-169">01</span><span class="sxs-lookup"><span data-stu-id="78cbf-169">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-170">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="78cbf-170">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="78cbf-171">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="78cbf-171">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="78cbf-172">01</span><span class="sxs-lookup"><span data-stu-id="78cbf-172">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-173">IsamType</span><span class="sxs-lookup"><span data-stu-id="78cbf-173">IsamType</span></span></p></td>
<td><p><span data-ttu-id="78cbf-174">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="78cbf-174">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="78cbf-175">2 </span><span class="sxs-lookup"><span data-stu-id="78cbf-175">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-176">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="78cbf-176">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="78cbf-177">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="78cbf-177">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="78cbf-178">00</span><span class="sxs-lookup"><span data-stu-id="78cbf-178">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-179">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="78cbf-179">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="78cbf-180">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="78cbf-180">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="78cbf-181">00</span><span class="sxs-lookup"><span data-stu-id="78cbf-181">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-182">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="78cbf-182">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="78cbf-183">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="78cbf-183">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="78cbf-p114">Importar dados do arquivo externo para o banco de dados atual. Alterar dados no banco de dados atual não os alterará no arquivo externo.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p114">Import data from the external file into the current database. Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-186">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="78cbf-186">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="78cbf-187">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="78cbf-187">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="78cbf-p115">Criar uma tabela no banco de dados atual vinculada ao arquivo externo. Alterar dados no banco de dados atual não os alterará no arquivo externo.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p115">Create a table in the current database that is linked to the external file. Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-190">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="78cbf-190">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="78cbf-191">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="78cbf-191">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="78cbf-p116">Exportar dados do banco de dados atual para um arquivo de texto. Esse processo substituirá os dados quando exportados para um arquivo já existente.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p116">Export data from the current database into a text file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-194">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="78cbf-194">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="78cbf-195">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="78cbf-195">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="78cbf-196">01</span><span class="sxs-lookup"><span data-stu-id="78cbf-196">01</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="78cbf-197">Ao alterar as configurações do Registro do Windows, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="78cbf-197">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="html-import-isam-formats"></a><span data-ttu-id="78cbf-198">HTML import ISAM formats</span><span class="sxs-lookup"><span data-stu-id="78cbf-198">HTML import ISAM formats</span></span>

<span data-ttu-id="78cbf-199">A **pasta importação \\ \\ HTML isam formats** do mecanismo de conectividade do Access contém as entradas a seguir.</span><span class="sxs-lookup"><span data-stu-id="78cbf-199">The **Access Connectivity Engine\\ISAM Formats\\HTML Import** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="78cbf-200">Nome da entrada</span><span class="sxs-lookup"><span data-stu-id="78cbf-200">Entry name</span></span></p></th>
<th><p><span data-ttu-id="78cbf-201">Tipo</span><span class="sxs-lookup"><span data-stu-id="78cbf-201">Type</span></span></p></th>
<th><p><span data-ttu-id="78cbf-202">Valor</span><span class="sxs-lookup"><span data-stu-id="78cbf-202">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-203">Mecanismo</span><span class="sxs-lookup"><span data-stu-id="78cbf-203">Engine</span></span></p></td>
<td><p><span data-ttu-id="78cbf-204">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="78cbf-204">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="78cbf-205">Texto</span><span class="sxs-lookup"><span data-stu-id="78cbf-205">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-206">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="78cbf-206">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="78cbf-207">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="78cbf-207">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="78cbf-208">Arquivos HTML (*.ht*)</span><span class="sxs-lookup"><span data-stu-id="78cbf-208">HTML Files (*.ht*)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-209">CanLink</span><span class="sxs-lookup"><span data-stu-id="78cbf-209">CanLink</span></span></p></td>
<td><p><span data-ttu-id="78cbf-210">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="78cbf-210">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="78cbf-211">01</span><span class="sxs-lookup"><span data-stu-id="78cbf-211">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-212">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="78cbf-212">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="78cbf-213">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="78cbf-213">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="78cbf-214">00</span><span class="sxs-lookup"><span data-stu-id="78cbf-214">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-215">IsamType</span><span class="sxs-lookup"><span data-stu-id="78cbf-215">IsamType</span></span></p></td>
<td><p><span data-ttu-id="78cbf-216">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="78cbf-216">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="78cbf-217">2 </span><span class="sxs-lookup"><span data-stu-id="78cbf-217">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-218">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="78cbf-218">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="78cbf-219">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="78cbf-219">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="78cbf-220">00</span><span class="sxs-lookup"><span data-stu-id="78cbf-220">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-221">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="78cbf-221">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="78cbf-222">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="78cbf-222">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="78cbf-223">00</span><span class="sxs-lookup"><span data-stu-id="78cbf-223">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-224">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="78cbf-224">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="78cbf-225">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="78cbf-225">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="78cbf-p117">Importar dados do arquivo externo para o banco de dados atual. Alterar dados no banco de dados atual não os alterará no arquivo externo.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p117">Import data from the external file into the current database. Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-228">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="78cbf-228">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="78cbf-229">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="78cbf-229">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="78cbf-p118">Criar uma tabela no banco de dados atual vinculada ao arquivo externo. Alterar dados no banco de dados atual não os alterará no arquivo externo.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p118">Create a table in the current database that is linked to the external file. Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-232">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="78cbf-232">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="78cbf-233">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="78cbf-233">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="78cbf-234">01</span><span class="sxs-lookup"><span data-stu-id="78cbf-234">01</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="78cbf-235">Ao alterar as configurações do Registro do Windows, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="78cbf-235">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="html-export-isam-formats"></a><span data-ttu-id="78cbf-236">FORMATOS ISAM de exportação HTML</span><span class="sxs-lookup"><span data-stu-id="78cbf-236">HTML export ISAM formats</span></span>

<span data-ttu-id="78cbf-237">A **pasta Exportação \\ \\ HTML isAM Formats** do Mecanismo de Conectividade do Access contém as entradas a seguir.</span><span class="sxs-lookup"><span data-stu-id="78cbf-237">The **Access Connectivity Engine\\ISAM Formats\\HTML Export** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="78cbf-238">Nome da entrada</span><span class="sxs-lookup"><span data-stu-id="78cbf-238">Entry name</span></span></p></th>
<th><p><span data-ttu-id="78cbf-239">Tipo</span><span class="sxs-lookup"><span data-stu-id="78cbf-239">Type</span></span></p></th>
<th><p><span data-ttu-id="78cbf-240">Valor</span><span class="sxs-lookup"><span data-stu-id="78cbf-240">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-241">Mecanismo</span><span class="sxs-lookup"><span data-stu-id="78cbf-241">Engine</span></span></p></td>
<td><p><span data-ttu-id="78cbf-242">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="78cbf-242">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="78cbf-243">Texto</span><span class="sxs-lookup"><span data-stu-id="78cbf-243">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-244">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="78cbf-244">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="78cbf-245">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="78cbf-245">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="78cbf-246">Arquivos HTML (\*.htm)</span><span class="sxs-lookup"><span data-stu-id="78cbf-246">HTML Files (\*.htm)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-247">CanLink</span><span class="sxs-lookup"><span data-stu-id="78cbf-247">CanLink</span></span></p></td>
<td><p><span data-ttu-id="78cbf-248">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="78cbf-248">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="78cbf-249">00</span><span class="sxs-lookup"><span data-stu-id="78cbf-249">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-250">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="78cbf-250">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="78cbf-251">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="78cbf-251">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="78cbf-252">01</span><span class="sxs-lookup"><span data-stu-id="78cbf-252">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-253">IsamType</span><span class="sxs-lookup"><span data-stu-id="78cbf-253">IsamType</span></span></p></td>
<td><p><span data-ttu-id="78cbf-254">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="78cbf-254">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="78cbf-255">2 </span><span class="sxs-lookup"><span data-stu-id="78cbf-255">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-256">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="78cbf-256">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="78cbf-257">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="78cbf-257">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="78cbf-258">00</span><span class="sxs-lookup"><span data-stu-id="78cbf-258">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-259">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="78cbf-259">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="78cbf-260">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="78cbf-260">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="78cbf-261">00</span><span class="sxs-lookup"><span data-stu-id="78cbf-261">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-262">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="78cbf-262">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="78cbf-263">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="78cbf-263">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="78cbf-p119">Exportar dados do banco de dados atual para um arquivo de texto. Esse processo substituirá os dados quando exportados para um arquivo já existente.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p119">Export data from the current database into a text file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-266">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="78cbf-266">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="78cbf-267">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="78cbf-267">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="78cbf-268">01</span><span class="sxs-lookup"><span data-stu-id="78cbf-268">01</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="78cbf-269">Ao alterar as configurações do Registro do Windows, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="78cbf-269">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a><span data-ttu-id="78cbf-270">Personalização do arquivo Schema.ini de texto e dados HTML</span><span class="sxs-lookup"><span data-stu-id="78cbf-270">Customizing the Schema.ini file for text and HTML data</span></span>

<span data-ttu-id="78cbf-p120">Para ler, importar ou exportar dados HTML e de texto, você precisa criar um arquivo Schema.ini, bem como incluir as informações ISAM do texto no arquivo .ini. O arquivo Schema.ini contém informações específicas da fonte de dados: como o arquivo de texto está formatado, como ele é lido no momento da importação e o formato de exportação padrão dos arquivos. Os exemplos a seguir mostram o layout de um arquivo de largura fixa, Filename.txt:</span><span class="sxs-lookup"><span data-stu-id="78cbf-p120">To read, import, or export text and HTML data, you need to create a Schema.ini file in addition to including the Text ISAM information in the .ini file. Schema.ini contains the specifics of a data source: how the text file is formatted, how it is read at import time, and what the default export format is for files. The following examples show the layout for a fixed-width file, Filename.txt:</span></span>

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

<span data-ttu-id="78cbf-274">Da mesma maneira, o formato de um arquivo delimitado é especificado assim:</span><span class="sxs-lookup"><span data-stu-id="78cbf-274">Similarly, the format for a delimited file is specified as follows:</span></span>

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

<span data-ttu-id="78cbf-275">Se estiver exportando dados para um arquivo de texto delimitado, especifique o formato desse arquivo também:</span><span class="sxs-lookup"><span data-stu-id="78cbf-275">If you are exporting data into a delimited text file, specify the format for that file as well:</span></span>

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

<span data-ttu-id="78cbf-p121">O exemplo My Special Export refere-se a uma opção de exportação específica; você pode determinar qualquer variação das opções de exportação no momento da conexão. Este último exemplo também corresponde ao nome da fonte de dados (DSN) que pode ser opcionalmente passado no momento da conexão. Todas as três seções de formato podem ser incluídas no arquivo .ini.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p121">The My Special Export example refers to a specific export option; you can specify any variation of export options at connect time. This last example also corresponds to a data source name (DSN) that can be optionally passed at connect time. All three format sections can be included in the same .ini file.</span></span>

<span data-ttu-id="78cbf-279">O mecanismo de banco de dados do Microsoft Access usa as entradas do Schema.ini da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="78cbf-279">The Microsoft Access database engine uses the Schema.ini entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="78cbf-280">Entrada</span><span class="sxs-lookup"><span data-stu-id="78cbf-280">Entry</span></span></p></th>
<th><p><span data-ttu-id="78cbf-281">Descrição</span><span class="sxs-lookup"><span data-stu-id="78cbf-281">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-282">ColNameHeader</span><span class="sxs-lookup"><span data-stu-id="78cbf-282">ColNameHeader</span></span></p></td>
<td><p><span data-ttu-id="78cbf-283">Pode ser <strong>True</strong> (indicando que o primeiro registro dos dados especifica os nomes das colunas) ou <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="78cbf-283">Can be set to either <strong>True</strong> (indicating that the first record of data specifies the column names) or <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-284">Formatar</span><span class="sxs-lookup"><span data-stu-id="78cbf-284">Format</span></span></p></td>
<td><p><span data-ttu-id="78cbf-285">Pode ser definido como um dos seguintes valores: TabDelimited, CSVDelimited, Delimited ( caractere único &lt; &gt; ) ou FixedLength.</span><span class="sxs-lookup"><span data-stu-id="78cbf-285">Can be set to one of the following values: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;), or FixedLength.</span></span> <span data-ttu-id="78cbf-286">O delimitador especificado para o formato de arquivo Delimitado pode ser qualquer caractere, exceto aspas duplas ( &quot; ).</span><span class="sxs-lookup"><span data-stu-id="78cbf-286">The delimiter specified for the Delimited file format can be any single character except a double quotation mark (&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-287">FixedFormat</span><span class="sxs-lookup"><span data-stu-id="78cbf-287">FixedFormat</span></span></p></td>
<td><p><span data-ttu-id="78cbf-288">Usado somente quando Format é FixedLength; pode ser definido como: RaggedEdge ou TrueFixedLength.</span><span class="sxs-lookup"><span data-stu-id="78cbf-288">Only used when the Format is FixedLength, this can be set to one of the following values: RaggedEdge or TrueFixedLength.</span></span> <span data-ttu-id="78cbf-289">RaggedEdge permite que as linhas terminem com um caractere de retorno de carro.</span><span class="sxs-lookup"><span data-stu-id="78cbf-289">RaggedEdge allows rows to be terminated with a Carriage Return character.</span></span> <span data-ttu-id="78cbf-290">TrueFixedLength exige que cada linha tenha um número exato de caracteres e qualquer caractere de retorno de carro que não estiver no limite da linha será considerado incorporado ao campo.</span><span class="sxs-lookup"><span data-stu-id="78cbf-290">TrueFixedLength requires each row to be an exact number of characters, and any Carriage Return characters not at a row boundary are assumed to be embedded in a field.</span></span> <span data-ttu-id="78cbf-291">Se essa configuração não estiver presente, o valor padrão será RaggedEdge.</span><span class="sxs-lookup"><span data-stu-id="78cbf-291">If this setting is not present, the default value is RaggedEdge.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-292">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="78cbf-292">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="78cbf-p124">Indica o número de linhas a serem verificadas ao determinar os tipos de dados da coluna. Se estiver definido como 0, o arquivo inteiro será pesquisado.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p124">Indicates the number of rows to be scanned when guessing the column data types. If this is set to 0, the entire file is searched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-295">CharacterSet</span><span class="sxs-lookup"><span data-stu-id="78cbf-295">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="78cbf-296">Pode ser definido como OEM, ANSI, UNICODE ou o número decimal de uma página de código válida e indica o conjunto de caracteres do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="78cbf-296">Can be set to OEM, ANSI, UNICODE, or the decimal number of a valid code page, and indicates the character set of the source file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-297">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="78cbf-297">DateTimeFormat</span></span></p></td>
<td><p><span data-ttu-id="78cbf-p125">Pode ser definida como uma cadeia de caracteres de formatação indicando datas e horas. Essa entrada deverá ser especificada se todos os campos de data/hora na importação/exportação forem tratados como sendo do mesmo formato. Há suporte para todos os formatos do mecanismo de banco de dados Microsoft Jet, com exceção de AM e PM. Na ausência de uma cadeia de caracteres de formatação, as opções de data e hora curtas do Painel de Controle do Windows serão usadas.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p125">Can be set to a format string indicating dates and times. This entry should be specified if all date/time fields in the import/export are handled with the same format. All of the Microsoft Jet database engine formats except AM and PM are supported. In the absence of a format string, the Windows Control Panel short date picture and time options are used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-302">CurrencySymbol</span><span class="sxs-lookup"><span data-stu-id="78cbf-302">CurrencySymbol</span></span></p></td>
<td><p><span data-ttu-id="78cbf-p126">Indica o símbolo de moeda a ser usado nos valores de moeda do arquivo de texto. Os exemplos incluem o símbolo do dólar ($) e Dm. Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p126">Indicates the currency symbol to be used for currency values in the text file. Examples include the dollar sign ($) and Dm. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-306">CurrencyPosFormat</span><span class="sxs-lookup"><span data-stu-id="78cbf-306">CurrencyPosFormat</span></span></p></td>
<td><p><span data-ttu-id="78cbf-307">Pode ser definido como qualquer um dos seguintes valores: Prefixo de símbolo de moeda sem separação ($1) Sufixo de símbolo de moeda sem separação (1$) Prefixo de símbolo de moeda com um sufixo de símbolo de moeda ($ 1) com separação de caracteres (1 $) Se essa entrada estiver ausente, o valor padrão no Painel de Controle do Windows será usado.</span><span class="sxs-lookup"><span data-stu-id="78cbf-307">Can be set to any of the following values: Currency symbol prefix with no separation ($1) Currency symbol suffix with no separation (1$) Currency symbol prefix with one character separation ($ 1) Currency symbol suffix with one character separation (1 $) If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-308">CurrencyDigits</span><span class="sxs-lookup"><span data-stu-id="78cbf-308">CurrencyDigits</span></span></p></td>
<td><p><span data-ttu-id="78cbf-p127">Especifica o número de dígitos usados na parte fracional do valor da moeda. Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p127">Specifies the number of digits used for the fractional part of a currency amount. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-311">CurrencyNegFormat</span><span class="sxs-lookup"><span data-stu-id="78cbf-311">CurrencyNegFormat</span></span></p></td>
<td><p><span data-ttu-id="78cbf-312">Pode ser um dos seguintes valores: ($1) –$1 $–1 $–1 – (1$) –1$ 1–$ 1$– –1 $ –$ 1 1 $– $ 1– $ –1 1 – $ ($ 1) (1 $) O cifrão é mostrado para este exemplo, mas deve ser substituído pelo valor currencySymbol apropriado no programa real.</span><span class="sxs-lookup"><span data-stu-id="78cbf-312">Can be one of the following values: ($1) –$1 $–1 $1– (1$) –1$ 1–$ 1$– –1 $ –$ 1 1 $– $ 1– $ –1 1– $ ($ 1) (1 $) The dollar sign is shown for purposes of this example, but it should be replaced with the appropriate CurrencySymbol value in the actual program.</span></span> <span data-ttu-id="78cbf-313">Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</span><span class="sxs-lookup"><span data-stu-id="78cbf-313">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-314">CurrencyThousandSymbol</span><span class="sxs-lookup"><span data-stu-id="78cbf-314">CurrencyThousandSymbol</span></span></p></td>
<td><p><span data-ttu-id="78cbf-p129">Indica o símbolo de um caractere a ser usado para separar os milhares dos valores de moeda no arquivo de texto. Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p129">Indicates the single-character symbol to be used for separating currency values by thousands in the text file. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-317">CurrencyDecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="78cbf-317">CurrencyDecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="78cbf-p130">Pode ser definido como qualquer caractere usado para separar a parte fracional do valor da moeda. Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p130">Can be set to any single character that is used to separate the whole from the fractional part of a currency amount. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-320">DecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="78cbf-320">DecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="78cbf-p131">Pode ser definido como qualquer caractere usado para separar o inteiro da parte fracional de um número. Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p131">Can be set to any single character that is used to separate the integer from the fractional part of a number. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-323">NumberDigits</span><span class="sxs-lookup"><span data-stu-id="78cbf-323">NumberDigits</span></span></p></td>
<td><p><span data-ttu-id="78cbf-p132">Indica o número de dígitos decimais usados na parte fracional de um número. Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</span><span class="sxs-lookup"><span data-stu-id="78cbf-p132">Indicates the number of decimal digits in the fractional portion of a number. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-326">NumberLeadingZeros</span><span class="sxs-lookup"><span data-stu-id="78cbf-326">NumberLeadingZeros</span></span></p></td>
<td><p><span data-ttu-id="78cbf-327">Especifica se um valor decimal inferior a 1 e superior a –1 deve conter zeros à esquerda; esse valor pode ser False (sem zeros à esquerda) ou True.</span><span class="sxs-lookup"><span data-stu-id="78cbf-327">Specifies whether a decimal value less than 1 and greater than –1 should contain leading zeros; this value can either be False (no leading zeros) or True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78cbf-328">Col1, Col2, ...</span><span class="sxs-lookup"><span data-stu-id="78cbf-328">Col1, Col2, …</span></span></p></td>
<td><p><span data-ttu-id="78cbf-329">Lista as colunas do arquivo de texto que devem ser lidas.</span><span class="sxs-lookup"><span data-stu-id="78cbf-329">Lists the columns in the text file to be read.</span></span> <span data-ttu-id="78cbf-330">O formato dessa entrada deve ser: <em>Coln</em> = <em>columnName</em> type [Width <em>#</em> ] <em>columnName:</em>os nomes das colunas com espaços incorporados devem ser incluídos entre aspas.</span><span class="sxs-lookup"><span data-stu-id="78cbf-330">The format of this entry should be: <em>Coln</em>=<em>columnName</em> type [Width <em>#</em>] <em>columnName</em>: Column names with embedded spaces should be enclosed in quotation marks.</span></span> <span data-ttu-id="78cbf-331"><em>type</em>: pode ser Bit, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime.</span><span class="sxs-lookup"><span data-stu-id="78cbf-331"><em>type</em>: Can be Bit, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime.</span></span> <span data-ttu-id="78cbf-332">Binary, OLE, Text ou Memo.</span><span class="sxs-lookup"><span data-stu-id="78cbf-332">Binary, OLE, Text, or Memo.</span></span> <span data-ttu-id="78cbf-333">Além disso, há suporte para os seguintes tipos de Driver de Texto ODBC: Char (mesmo que Text) Float <em></em> (mesmo que Double) Integer (mesmo que Short) LongChar (mesmo que Memo) No caso de um tipo Memorando, um marcador de formato adicional [Hiperlink de Atributo] pode ser usado para especificar colunas que devem ser URLs ativas no Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="78cbf-333">In addition, the following ODBC Text Driver types are supported: Char (same as Text) Float (same as Double) Integer (same as Short) LongChar (same as Memo) Date <em>date format</em> In the case of a Memo type an additional format marker [Attribute Hyperlink] can be used to specify columns that should be active URLs in Microsoft Access.</span></span> <span data-ttu-id="78cbf-334">No caso de um tipo Decimal, marcadores de formato adicionais [Scale #] Precision #] devem ser usados.</span><span class="sxs-lookup"><span data-stu-id="78cbf-334">In the case of a Decimal type the additional format markers [Scale #] Precision #] should be used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78cbf-335">TextDelimiter</span><span class="sxs-lookup"><span data-stu-id="78cbf-335">TextDelimiter</span></span></p></td>
<td><p><span data-ttu-id="78cbf-336">Pode ser qualquer caractere usado para delimitar cadeias de caracteres que contenham qualquer um dos outros caracteres especiais.</span><span class="sxs-lookup"><span data-stu-id="78cbf-336">Can be set to any single character that is used to delimit strings that contain any of the other special characters.</span></span> <span data-ttu-id="78cbf-337">Por exemplo</span><span class="sxs-lookup"><span data-stu-id="78cbf-337">E.g.</span></span> <span data-ttu-id="78cbf-338">&quot;abc , xyz,pqr , hij Se essa entrada não estiver presente, o &quot; &quot; &quot; &quot; &quot; delimiter padrão será aspas duplas.</span><span class="sxs-lookup"><span data-stu-id="78cbf-338">&quot;abc&quot;,&quot;xyz,pqr&quot;,&quot;hij&quot; If this entry is not present the default delimiter is a double quote.</span></span> <span data-ttu-id="78cbf-339">Se essa entrada for a cadeia de &quot; &quot; caracteres, nenhum caractere será tratado como delimitadores.</span><span class="sxs-lookup"><span data-stu-id="78cbf-339">If this entry is the string &quot;none&quot; then no characters will be treated as delimiters.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="78cbf-340">[!OBSERVAçãO] Ao alterar as configurações do arquivo Schema.ini, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="78cbf-340">When you change Schema.ini file settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>


