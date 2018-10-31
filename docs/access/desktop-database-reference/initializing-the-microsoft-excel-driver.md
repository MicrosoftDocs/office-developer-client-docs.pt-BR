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
ms.openlocfilehash: 85961b761255583738026113a025d6ca84b61f83
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861985"
---
# <a name="initializing-the-microsoft-excel-driver"></a>Inicializando o driver do Microsoft Excel

**Aplica-se a**: Access 2013 | Office 2013

Quando você instala o driver do Excel, o programa de instalação grava um conjunto de valores padrão no registro do Windows nas subchaves mecanismos e ISAM Formats. Você não deve modificar essas configurações diretamente; use o programa de instalação de seu aplicativo para adicionar, remover ou alterar essas configurações. As seções a seguir descrevem a inicialização e as configurações do ISAM Format no driver de banco de dados do Microsoft Excel.

## <a name="excel-initialization-settings"></a>Configurações de inicialização do Excel

O **mecanismo de conectividade do Access\\mecanismos\\Excel** pasta inclui configurações de inicialização para o driver Aceexcl.dll, usada para acesso externo às planilhas do Microsoft Excel. As configurações normais das entradas nessa pasta são mostradas no exemplo a seguir.

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

O mecanismo de banco de dados do Microsoft Access usa as entradas da pasta do Excel da seguinte maneira:

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
<td><p>A localização do arquivo msexcl40. O caminho completo é determinado no momento da instalação. Os valores são do tipo REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>Registo TypeGuessRows</p></td>
<td><p>O número de linhas a serem verificadas para o tipo de dados. O tipo de dados é determinado dado o número máximo de tipos de dados encontrados. Se houver uma ligação, o tipo de dados é determinado na seguinte ordem: número, moeda, data, texto, Boolean. Se forem encontrados dados que não coincide com o tipo de dados avaliado para a coluna, ele é retornado como um valor <strong>Nulo</strong> . Na importação, se uma coluna tiver mistos tipos de dados, toda a coluna será convertida de acordo com a configuração ImportMixedTypes. O número padrão de linhas a serem verificadas é 8. Os valores são do tipo REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>ImportMixedTypes</p></td>
<td><p>Pode ser definido como MajorityType ou Text. Se for definido como MajorityType, as colunas com tipos de dados mistos serão calculadas conforme o tipo de dados predominante na importação. Se for definido como Text, as colunas de tipos de dados mistos serão calculadas como Text na importação. O padrão é Text. Os valores são do tipo REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>AppendBlankRows</p></td>
<td><p>O número de linhas em branco a serem acrescentadas ao final de uma planilha da versão 3.5 ou 4.0 antes da adição de novos dados. Por exemplo, se AppendBlankRows for definido como, o Microsoft Jet acrescentará 4 linhas em branco ao final da planilha antes de acrescentar linhas que contenham dados. Valores inteiros nessa configuração podem variar de 0 a 16; o padrão é 01 (uma linha adicional acrescentada). Os valores são do tipo REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>FirstRowHasNames</p></td>
<td><p>Um valor binário que indica se a primeira linha da tabela contém nomes de coluna. O valor 01 indica que, durante a importação, os nomes de coluna são extraídos da primeira linha. O valor 00 indica nenhum nome de coluna na primeira linha; os nomes de coluna aparecem como F1, F2, F3 etc. O padrão é 01. Os valores são do tipo REG_BINARY.</p></td>
</tr>
</tbody>
</table>


O **mecanismo de conectividade do Access\\mecanismos\\Excel 8.0** pasta contém as entradas a seguir, que se aplicam ao Microsoft Excel 97.

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
<td><p>Excel</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Microsoft Excel 97-2000 (*.xls)</p></td>
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
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exportar dados do banco de dados atual para um arquivo do Microsoft Excel 97. Esse processo substituirá os dados quando exportados para um arquivo já existente.</p></td>
</tr>
<tr class="odd">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> Ao alterar as configurações do Registro do Windows, você deve fechar e reiniciar o mecanismo de banco de dados para que as novas configurações entrem em vigor.

## <a name="see-also"></a>Confira também

[Usando a configuração de registo TypeGuessRows para o Driver do Excel](https://support.office.com/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b)
