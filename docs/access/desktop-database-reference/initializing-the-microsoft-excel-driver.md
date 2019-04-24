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
ms.openlocfilehash: c3424fd4b85108120ea4accc2dfa65d55394f0d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291432"
---
# <a name="initializing-the-microsoft-excel-driver"></a>Inicialização do driver do Microsoft Excel

**Aplica-se a**: Excel 2016 | Access 2016 | Access 2013 | Office 2013 | Excel 2013 | Office for Business Access 2013 | Excel 2010 | Access 2010

Quando você instala o driver do Excel, o programa de instalação grava um conjunto de valores padrão no registro do Windows nas subchaves Engines e ISAM formats. Você não deve modificar essas configurações diretamente; use o programa de instalação de seu aplicativo para adicionar, remover ou alterar essas configurações. As seções a seguir descrevem a inicialização e as configurações do ISAM Format no driver de banco de dados do Microsoft Excel.

## <a name="excel-initialization-settings"></a>Configurações de inicialização do Excel

A pasta do **Excel\\mecanismos\\do mecanismo de conectividade do Access** inclui configurações de inicialização para o driver Aceexcl. dll, usado para acesso externo às planilhas do Microsoft Excel. As configurações normais das entradas nessa pasta são mostradas no exemplo a seguir.

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
<td><p>Win</p></td>
<td><p>A localização do arquivo msexcl40. O caminho completo é determinado no momento da instalação. Os valores são do tipo REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>TypeGuessRows</p></td>
<td><p>O número de linhas cujo tipo de dados será verificado. O tipo de dados é determinado pelo número máximo de tipos de dados localizados. Se houver alguma ligação, o tipo de dados será determinado na seguinte ordem: número, moeda, data, texto e booleano. Se forem encontrados dados que não correspondam ao tipo desejado para a coluna, ele serão retornados como um valor <strong>Nulo</strong>. Na importação, se uma coluna tiver tipos de dados mistos, a coluna toda será calculada conforme a configuração de ImportMixedTypes. O número padrão de linhas a serem verificadas é 8. Os valores são do tipo REG_DWORD.</p></td>
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

<br/>

A pasta **mecanismos\\\\de mecanismo de conectividade do Microsoft Excel 8,0** contém as entradas a seguir, que se aplicam ao Microsoft Excel 97.

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
<td><p>Mecanismo</p></td>
<td><p>REG_SZ</p></td>
<td><p>Excel</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Microsoft Excel 97-2000 (*.xls)</p></td>
</tr>
<tr class="odd">
<td><p>CanVinculo</p></td>
<td><p>REG_BINARY</p></td>
<td><p>0,01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>Isamtype</p></td>
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
<td><p>0,01</p></td>
</tr>
<tr class="even">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exportar dados do banco de dados atual para um arquivo do Microsoft Excel 97. Esse processo substituirá os dados quando exportados para um arquivo já existente.</p></td>
</tr>
<tr class="odd">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>0,01</p></td>
</tr>
</tbody>
</table>


## <a name="using-the-typeguessrows-setting-for-excel-driver"></a>Usando a configuração TypeGuessRows para o driver do Excel
Ao usar o driver do Microsoft Excel, você pode usar o valor de registro **TypeGuessRows** para configurar quantas linhas devem ser verificadas quanto ao tipo de dados. O valor **TypeGuessRows** está localizado na seguinte subchave do registro:

# <a name="office-2016taboffice-2016"></a>[Office 2016](#tab/office-2016)

Para uma instalação MSI do Office

- Para o Office de 32 bits no Windows de 32 bits ou no Office de 64 bits no Windows de 64 bits:
    
  **Engine\Engines\Excel de conectividade HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access**

- Para o Office de 32 bits em Windows de 64 bits:

  **Engine\Engines\Excel de conectividade HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access**
    
Para uma instalação clique para executar do Office

- Para o Office de 32 bits no Windows de 32 bits ou no Office de 64 bits no Windows de 64 bits:
    
  **Engine\Engines\Excel de conectividade HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access**

- Para o Office de 32 bits em Windows de 64 bits:
    
  **Engine\Engines\Excel de conectividade HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access**

O número padrão de linhas a serem verificadas é **8** (oito). Quando você define o valor de **TypeGuessRows** para **0** (zero), o driver do Excel verifica as primeiras 16.384 linhas para o tipo de dados. Se você deseja verificar mais de 16.384 linhas, defina **TypeGuessRows** como um valor que se baseia no intervalo desejado. Para verificar todas as linhas, defina **TypeGuessRows** como 1.048.576 (o número máximo de linhas permitido no Excel).
 
O tipo de dados é determinado pelo número máximo de tipos de dados que é encontrado. Se houver um empate, o tipo de dados será determinado na seguinte ordem:

- Número
- Moeda
- Data
- Texto
- Booliano

Se forem encontrados dados que não correspondam ao tipo de dados adivinhados para a coluna, esses dados serão retornados como um valor **nulo** . Durante uma importação, se uma coluna tem tipos de dados mistos, toda a coluna é convertida para o tipo de dados definido pela configuração **ImportMixedTypes** .

# <a name="office-2013taboffice-2013"></a>[Office 2013](#tab/office-2013)

Para o Office de 32 bits no Windows de 32 bits ou no Office de 64 bits no Windows de 64 bits:

**Engine\Engines\Excel de conectividade HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access**

Para o Office de 32 bits em Windows de 64 bits:

**Engine\Engines\Excel de conectividade HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access**

O número padrão de linhas a serem verificadas é **8** (oito). Quando você define o valor de **TypeGuessRows** para **0** (zero), o driver do Excel verifica as primeiras 16.384 linhas para o tipo de dados. Se você deseja verificar mais de 16.384 linhas, defina **TypeGuessRows** como um valor que se baseia no intervalo desejado. Para verificar todas as linhas, defina **TypeGuessRows** como 1.048.576 (o número máximo de linhas permitido no Excel).
 
O tipo de dados é determinado pelo número máximo de tipos de dados que é encontrado. Se houver um empate, o tipo de dados será determinado na seguinte ordem:

- Número
- Moeda
- Data
- Texto
- Booliano

Se forem encontrados dados que não correspondam ao tipo de dados adivinhados para a coluna, esses dados serão retornados como um valor **nulo** . Durante uma importação, se uma coluna tem tipos de dados mistos, toda a coluna é convertida para o tipo de dados definido pela configuração **ImportMixedTypes** .

# <a name="office-2010taboffice-2010"></a>[Office 2010](#tab/office-2010)

Para o Office de 32 bits no Windows de 32 bits ou no Office de 64 bits no Windows de 64 bits:

**Engine\Engines\Excel de conectividade HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access**

Para o Office de 32 bits em Windows de 64 bits:

**Engine\Engines\Excel de conectividade HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access**

O número padrão de linhas a serem verificadas é **8** (oito). Quando você define o valor de **TypeGuessRows** para **0** (zero), o driver do Excel verifica as primeiras 16.384 linhas para o tipo de dados. Se você deseja verificar mais de 16.384 linhas, defina **TypeGuessRows** como um valor que se baseia no intervalo desejado. Para verificar todas as linhas, defina **TypeGuessRows** como 1.048.576 (o número máximo de linhas permitido no Excel).
 
O tipo de dados é determinado pelo número máximo de tipos de dados que é encontrado. Se houver um empate, o tipo de dados será determinado na seguinte ordem:

- Número
- Moeda
- Data
- Texto
- Booliano

Se forem encontrados dados que não correspondam ao tipo de dados adivinhados para a coluna, esses dados serão retornados como um valor **nulo** . Durante uma importação, se uma coluna tem tipos de dados mistos, toda a coluna é convertida para o tipo de dados definido pela configuração **ImportMixedTypes** .

---
> [!NOTE]
> [!OBSERVAçãO] When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.

## <a name="see-also"></a>Confira também

- [Usando a configuração TypeGuessRows para o driver do Excel](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)

