---
title: Bloco de dados ParaCadaRegistro
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84ab685b946e390645027790e5b1402561527ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292325"
---
# <a name="foreachrecord-data-block"></a>Bloco de dados ParaCadaRegistro

**Aplica-se ao:** Access 2013, Office 2013

Um bloco de dados **ParaCadaRegistro** repete um conjunto de instruções para cada registro em um domínio.

> [!NOTE]
> O bloco de dados **ParaCadaRegistro** está disponível somente em Macros de Dados.

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
<th><p>Argument</p></th>
<th><p>Obrigatório</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>No</strong></p></td>
<td><p>Sim</p></td>
<td><p>Uma cadeia de caracteres que identifica o domínio de registros a ser utilizado. O argumento <em>in</em> pode conter o nome da tabela, uma consulta seleção ou uma instrução SQL.</p><p><strong>Observação</strong>: o domínio especificado não pode incluir dados armazenados em uma tabela vinculada ou fonte de dados ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong>Condição Where</strong></p></td>
<td><p>Não</p></td>
<td><p>Uma expressão de cadeia de caracteres usada para restringir o intervalo de dados no qual o bloco de dados <strong>ParaCadaRegistro</strong> é executado. Por exemplo, os critérios geralmente são equivalentes à cláusula WHERE em uma expressão SQL, sem a palavra WHERE. Se criteria for omitido, o bloco de dados <strong>ParaCadaRegistro</strong> funcionará em todo o domínio especificado pelo argumento <em>in</em> . Qualquer campo incluído nos critérios também deve ser um campo em <em>Em</em>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>Não</p></td>
<td><p>Uma cadeia de caracteres que fornece um nome alternativo para o domínio especificado pelo argumento <em>in</em> . Frequentemente usado para reduzir o nome da tabela para referências subsequentes para evitar possíveis referências ambíguas. Se <em>alias</em> não for especificado, o nome da tabela ou da consulta será usado como o alias.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Use a ação **[SairparaCadaRegistro](exitforeachrecord-macro-action.md)** para encerrar um bloco de dados **ParaCadaRegistro** imediatamente.

