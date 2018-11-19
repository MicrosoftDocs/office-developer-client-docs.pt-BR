---
title: Bloco de dados ParaCadaRegistro
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a627804676ad4e61c5eef050c5bc12c36b9e6d1a
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026229"
---
# <a name="foreachrecord-data-block"></a>Bloco de dados ParaCadaRegistro

**Aplica-se a**: Access 2013, o Office 2013

Um bloco de dados **ParaCadaRegistro** repete um conjunto de instruções para cada registro em um domínio.

> [!NOTE]
> [!OBSERVAçãO] O bloco de dados **ParaCadaRegistro** está disponível somente em Macros de Dados.

## <a name="setting"></a>Configuração

A ação **ParaCadaRegistro** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Obrigatório</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Em</strong></p></td>
<td><p>Sim</p></td>
<td><p>Uma cadeia de caracteres que identifica o domínio de registros para operar em. O argumento <em>em</em> pode conter o nome da tabela, uma consulta seleção ou uma instrução SQL.</p><p><strong>Observação</strong>: O domínio especificado não pode incluir dados armazenados em uma tabela vinculada ou fonte de dados ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong>Condição Where</strong></p></td>
<td><p>Não</p></td>
<td><p>Uma expressão de cadeia de caracteres usada para restringir o intervalo de dados no qual o bloco de dados <strong>ParaCadaRegistro</strong> é executada. Por exemplo, critérios costuma ser equivalente à cláusula WHERE em uma expressão SQL, sem a palavra onde. Se os critérios for omitido, o bloco de dados <strong>ParaCadaRegistro</strong> opera em todo o domínio especificado pelo argumento <em>em</em> . Qualquer campo que está incluído nos critérios também deve ser um campo no <em>In</em>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>Não</p></td>
<td><p>Uma cadeia de caracteres que fornece um nome alternativo para o domínio especificado pelo argumento <em>em</em> . Frequentemente usado para reduzir o nome da tabela referências posteriores evitar possíveis referências ambíguas. Se o <em>Alias</em> não for especificado, o nome da tabela ou consulta será usado como o alias.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Use a ação **[SairparaCadaRegistro](exitforeachrecord-macro-action.md)** para encerrar um bloco de dados **ParaCadaRegistro** imediatamente.

