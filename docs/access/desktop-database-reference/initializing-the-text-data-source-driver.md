---
title: Inicializando o driver da fonte de dados de texto
TOCTitle: Initializing the Text Data Source Driver
ms:assetid: cba0864e-5f94-bf43-4708-b1981e3acaff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834391(v=office.15)
ms:contentKeyID: 48547718
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032166
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fb897c4e057b767c98676bc14c9f1e70c22095ee
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464176"
---
# <a name="initializing-the-text-data-source-driver"></a>Inicializando o driver da fonte de dados de texto


**Aplica-se a**: Access 2013 | Office 2013


O mesmo driver de banco de dados é usado para fontes de dados HTML e de texto.

Quando você instala o driver de banco de dados da fonte de dados de texto, o programa de instalação grava um conjunto de valores padrão no Registro do Microsoft® Windows®, nas subchaves Engines e ISAM Formats. Você não deve modificar essas configurações diretamente; use o programa de instalação de seu aplicativo para adicionar, remover ou alterar essas configurações. As seções a seguir descrevem a inicialização e as configurações do ISAM Format no driver de banco de dados da fonte de dados de texto.

## <a name="text-data-source-initialization-settings"></a>Configurações de inicialização da fonte de dados de texto

O **mecanismo de conectividade do Access\\ISAM Formats\\pasta texto** inclui configurações de inicialização para o driver Acetxt.dll, usadas para acesso externo para arquivos de dados de texto. As configurações normais das entradas nessa pasta são mostradas no exemplo a seguir.

```vb
    win32=<path>\ ACETXT.DLL 
    
    MaxScanRows=25 
    
    FirstRowHasNames=True 
    
    CharacterSet= ANSI 
    
    Format=CSVDelimited 
    
    Extensions= txt,csv,tab,asc 
    
    ExportCurrencySymbols=Yes
```

O mecanismo de banco de dados do Microsoft Access usa as entradas da pasta Text da seguinte maneira:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Entrada</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Win32</p></td>
<td><p>A localização do arquivo Acetxt.dll. O caminho completo é determinado no momento da instalação. Os valores são do tipo REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>MaxScanRows</p></td>
<td><p>O número de linhas a serem verificadas ao determinar os tipos de coluna. Se for 0, o arquivo inteiro será pesquisado. O padrão é 25. Os valores são do tipo REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>FirstRowHasNames</p></td>
<td><p>Um valor binário que indica se a primeira linha da tabela contém nomes de coluna. Um valor 0 indica que, durante a importação, os nomes de coluna serão extraídos da primeira linha.</p></td>
</tr>
<tr class="even">
<td><p>CharacterSet</p></td>
<td><p>Um indicador de como as páginas de texto são armazenadas. As configurações possíveis são:</p>
<p></p>
<ul>
<li><p>ANSI — a página de código ANSI do computador. São feitas as conversões AnsiToUnicode e UnicodeToAnsi.</p></li>
<li><p>OEM — a página de código OEM do computador. São feitas as conversões OemToUnicode e UnicodeToOem.</p></li>
<li><p>Unicode — não são feitas conversões de página de código.</p></li>
<li><p>&lt;número decimal&gt; — o número de página de código de um conjunto de caracteres específica. Conversões de e para Unicode serão feitos.</p></li>
</ul>
<p></p>
<p>O padrão é ANSI. Os valores são do tipo REG_SZ.</p></td>
</tr>
<tr class="odd">
<td><p>Format</p></td>
<td><p>Pode ser qualquer um dos seguintes: TabDelimited, CSVDelimited, delimitado (&lt;caractere único&gt;). O delimitador caractere único no formato delimitado pode ser qualquer caractere único, exceto aspas duplas (&quot;). O padrão é CSVDelimited. Os valores são do tipo REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>Extensions</p></td>
<td><p>A extensão de qualquer arquivo a ser pesquisado ao procurar dados baseados em texto. O padrão é txt, csv, tab, asc. Os valores são do tipo REG_SZ.</p></td>
</tr>
<tr class="odd">
<td><p>ExportCurrencySymbols</p></td>
<td><p>Um valor binário que indica se o símbolo de moeda apropriado é incluído quando os campos de moeda são exportados. Um valor 01 indica que o símbolo é incluído. Um valor 00 indica que apenas os dados numéricos são exportados. O valor padrão é 01. Os valores são do tipo REG_BINARY.</p></td>
</tr>
</tbody>
</table>


## <a name="text-data-source-isam-formats"></a>ISAM Formats da fonte de dados de texto

O **mecanismo de conectividade do Access\\ISAM Formats\\texto** pasta contém as entradas a seguir.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da entrada</p></th>
<th><p>Tipo</p></th>
<th><p>Valor</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
<td><p>REG_SZ</p></td>
<td><p>Texto</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Arquivos de texto (*.txt; *.csv; *.tab; *.asc)</p></td>
</tr>
<tr class="odd">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Arquivos de texto (*.txt; *.csv; *.tab; *.asc)</p></td>
</tr>
<tr class="even">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="odd">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>2</p></td>
</tr>
<tr class="odd">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextImport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Importar dados do arquivo externo para o banco de dados atual. Alterar dados no banco de dados atual não os alterará no arquivo externo.</p></td>
</tr>
<tr class="even">
<td><p>ResultTextLink</p></td>
<td><p>REG_SZ</p></td>
<td><p>Criar uma tabela no banco de dados atual vinculada ao arquivo externo. Alterar dados no banco de dados atual não os alterará no arquivo externo.</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exportar dados do banco de dados atual para um arquivo de texto. Esse processo substituirá os dados quando exportados para um arquivo já existente.</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>Ao alterar as configurações do Registro do Windows, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.</P>



## <a name="html-import-isam-formats"></a>ISAM Formats para HTML Import

O **mecanismo de conectividade do Access\\ISAM Formats\\HTML Import** pasta contém as entradas a seguir.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da entrada</p></th>
<th><p>Tipo</p></th>
<th><p>Valor</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
<td><p>REG_SZ</p></td>
<td><p>Texto</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Arquivos HTML (*. HT*)</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>ResultTextImport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Importar dados do arquivo externo para o banco de dados atual. Alterar dados no banco de dados atual não os alterará no arquivo externo.</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextLink</p></td>
<td><p>REG_SZ</p></td>
<td><p>Criar uma tabela no banco de dados atual vinculada ao arquivo externo. Alterar dados no banco de dados atual não os alterará no arquivo externo.</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>Ao alterar as configurações do Registro do Windows, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.</P>



## <a name="html-export-isam-formats"></a>ISAM Formats para HTML Export

O **mecanismo de conectividade do Access\\ISAM Formats\\HTML Export** pasta contém as entradas a seguir.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da entrada</p></th>
<th><p>Tipo</p></th>
<th><p>Valor</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
<td><p>REG_SZ</p></td>
<td><p>Texto</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Arquivos HTML (*.htm)</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exportar dados do banco de dados atual para um arquivo de texto. Esse processo substituirá os dados quando exportados para um arquivo já existente.</p></td>
</tr>
<tr class="odd">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>Ao alterar as configurações do Registro do Windows, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.</P>



## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a>Personalizando o arquivo Schema.ini para dados HTML e de texto

Para ler, importar ou exportar dados HTML e de texto, você precisa criar um arquivo Schema.ini, bem como incluir as informações ISAM do texto no arquivo .ini. O arquivo Schema.ini contém informações específicas da fonte de dados: como o arquivo de texto está formatado, como ele é lido no momento da importação e o formato de exportação padrão dos arquivos. Os exemplos a seguir mostram o layout de um arquivo de largura fixa, Filename.txt:

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

Da mesma maneira, o formato de um arquivo delimitado é especificado assim:

```text
    [Delimit.txt] 
    
    ColNameHeader=True 
    
    Format=Delimited() 
    
    MaxScanRows=0 
    
    CharacterSet=OEM 
    
    Col1=username char width 50 
    
    Col2=dateofbirth Date width 9
```

Se estiver exportando dados para um arquivo de texto delimitado, especifique o formato desse arquivo também:

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

O exemplo My Special Export refere-se a uma opção de exportação específica; você pode determinar qualquer variação das opções de exportação no momento da conexão. Este último exemplo também corresponde ao nome da fonte de dados (DSN) que pode ser opcionalmente passado no momento da conexão. Todas as três seções de formato podem ser incluídas no arquivo .ini.

O mecanismo de banco de dados do Microsoft Access usa as entradas do Schema.ini da seguinte maneira:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Entrada</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ColNameHeader</p></td>
<td><p>Pode ser <strong>True</strong> (indicando que o primeiro registro dos dados especifica os nomes das colunas) ou <strong>False</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Formatar</p></td>
<td><p>Pode ser definido como um dos seguintes valores: TabDelimited, CSVDelimited, delimitado (&lt;caractere único&gt;), ou FixedLength. O delimitador especificado para o formato de arquivo delimitado pode ser qualquer caractere único, exceto aspas duplas (&quot;).</p></td>
</tr>
<tr class="odd">
<td><p>FixedFormat</p></td>
<td><p>Usado somente quando Format é FixedLength; pode ser definido como: RaggedEdge ou TrueFixedLength.
 RaggedEdge permite que as linhas terminem com um caractere de retorno de carro. TrueFixedLength exige que cada linha tenha um número exato de caracteres e qualquer caractere de retorno de carro que não estiver no limite da linha será considerado incorporado ao campo. Se essa configuração não estiver presente, o valor padrão será RaggedEdge.</p></td>
</tr>
<tr class="even">
<td><p>MaxScanRows</p></td>
<td><p>Indica o número de linhas a serem verificadas ao determinar os tipos de dados da coluna. Se estiver definido como 0, o arquivo inteiro será pesquisado.</p></td>
</tr>
<tr class="odd">
<td><p>CharacterSet</p></td>
<td><p>Pode ser definido como OEM, ANSI, UNICODE ou o número decimal de uma página de código válida e indica o conjunto de caracteres do arquivo de origem.</p></td>
</tr>
<tr class="even">
<td><p>DateTimeFormat</p></td>
<td><p>Pode ser definida como uma cadeia de caracteres de formatação indicando datas e horas. Essa entrada deverá ser especificada se todos os campos de data/hora na importação/exportação forem tratados como sendo do mesmo formato. Há suporte para todos os formatos do mecanismo de banco de dados Microsoft Jet, com exceção de AM e PM. Na ausência de uma cadeia de caracteres de formatação, as opções de data e hora curtas do Painel de Controle do Windows serão usadas.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencySymbol</p></td>
<td><p>Indica o símbolo de moeda a ser usado nos valores de moeda do arquivo de texto. Os exemplos incluem o símbolo do dólar ($) e Dm. Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyPosFormat</p></td>
<td><p>Pode ser definido como qualquer um dos seguintes valores: prefixo de símbolo de moeda com o sufixo de símbolo de moeda sem separação ($1) sem separação (1$) prefixo de símbolo de moeda com o sufixo de símbolo de moeda de separação ($ 1) de um caractere com separação de um caractere (1 $) se essa entrada não estiver presente, o valor padrão no painel de controle do Windows é usado.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencyDigits</p></td>
<td><p>Especifica o número de dígitos usados na parte fracional do valor da moeda. Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyNegFormat</p></td>
<td><p>Pode ser um dos seguintes valores: ($1) – $1 $– 1 $1 – (1$) – 1$ $ 1 a US $ 1 – – 1 $ – $ 1 1 $– $ 1 – $ – 1 1 – $ ($ 1) (1 $) cifrão é mostrado para os fins deste exemplo, mas deveria ser substituído pelo valor CurrencySymbol apropriado no programa real. Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencyThousandSymbol</p></td>
<td><p>Indica o símbolo de um caractere a ser usado para separar os milhares dos valores de moeda no arquivo de texto. Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyDecimalSymbol</p></td>
<td><p>Pode ser definido como qualquer caractere usado para separar a parte fracional do valor da moeda. Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</p></td>
</tr>
<tr class="odd">
<td><p>DecimalSymbol</p></td>
<td><p>Pode ser definido como qualquer caractere usado para separar o inteiro da parte fracional de um número. Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</p></td>
</tr>
<tr class="even">
<td><p>NumberDigits</p></td>
<td><p>Indica o número de dígitos decimais usados na parte fracional de um número. Na ausência dessa entrada, o valor padrão do Painel de Controle do Windows será usado.</p></td>
</tr>
<tr class="odd">
<td><p>NumberLeadingZeros</p></td>
<td><p>Especifica se um valor decimal inferior a 1 e superior a –1 deve conter zeros à esquerda; esse valor pode ser False (sem zeros à esquerda) ou True.</p></td>
</tr>
<tr class="even">
<td><p>Col1, Col2, …</p></td>
<td><p>Lista as colunas no arquivo de texto a ser lido. O formato dessa entrada deve ser: <em>Coln</em>=<em>columnName</em> tipo [largura <em> #</em>] <em>columnName</em>: nomes de colunas com espaços incorporados devem estar entre aspas. <em>tipo</em>: pode ser Bit, Byte, Short, Long, Decimal, moeda, único, duplo, data/hora. Binário, OLE, texto ou Memorando. Além disso, os seguintes tipos de Driver de texto ODBC são suportados: Char (mesmo que Text) Float (mesmo que Double) Integer (mesmo que Short) LongChar (mesmo que Memo) Date <em>formato de data</em> no caso de um marcador de formato adicional [Attribute Hyperlink] pode ser um tipo de memorando usado para especificar as colunas que devem ser URLs ativas no Microsoft Access. No caso de um tipo Decimal, marcadores de formato adicionais [Scale #] Precision #] devem ser usados.</p></td>
</tr>
<tr class="odd">
<td><p>TextDelimiter</p></td>
<td><p>Pode ser qualquer caractere usado para delimitar cadeias de caracteres que contenham qualquer um dos outros caracteres especiais.
 E.g. &quot;ABC&quot;,&quot;xyz, pqr&quot;,&quot;hij&quot; se essa entrada não estiver presente o delimitador padrão será as aspas duplas. Se essa entrada é a cadeia de caracteres &quot;nenhum&quot; e nenhum caractere será tratado como delimitadores.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> [!OBSERVAçãO] Ao alterar as configurações do arquivo Schema.ini, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.


