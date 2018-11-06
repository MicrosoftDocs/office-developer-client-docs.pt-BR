---
title: Ação da macro ExecutarSQL
TOCTitle: RunSQL macro action
ms:assetid: 3692142d-f8a8-e194-0b38-051167f46319
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192476(v=office.15)
ms:contentKeyID: 48544174
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12983
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0527f5a55235fa36725152d228dfd2294c63bf53
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996871"
---
# <a name="runsql-macro-action"></a>Ação da macro ExecutarSQL

**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **ExecutarSQL** para executar uma consulta ação Access usando a instrução SQL correspondente. Pode também executar uma consulta de definição de dados.

> [!NOTE]
> [!OBSERVAçãO] This action will not be allowed if the database is not trusted. 

## <a name="setting"></a>Configuração

A ação **ExecutarSQL** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento da ação</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Instrução SQL</strong></p></td>
<td><p>A instrução SQL da consulta ação ou da consulta de definição de dados a ser executada. O tamanho máximo dessa instrução é de 255 caracteres. Este é um argumento obrigatório.</p></td>
</tr>
<tr class="even">
<td><p><strong>Usar transação</strong></p></td>
<td><p>Selecione <strong>Sim</strong> para incluir essa consulta em uma transação. Selecione <strong>Não</strong> se não quiser usar uma transação. O padrão é <strong>Sim</strong>. Se você selecionar <strong>Não</strong> para este argumento, a consulta poderá ser executada mais rapidamente.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode usar consultas ação para acrescentar, excluir e atualizar registros e para salvar o conjunto de resultados de uma consulta como uma nova tabela. As consultas de definições de dados podem ser usadas para criar, alterar e excluir tabelas, e para criar e excluir índices. Use a ação **ExecutarSQL** para executar essas operações diretamente em uma macro, sem precisar usar consultas armazenadas.

Se precisar digitar uma instrução SQL com mais de 255 caracteres, use o método **RunSQL** do objeto **DoCmd** em um módulo do VBA (Visual Basic for Applications). No VBA, é possível digitar instruções SQL com até 32.768 caracteres.

As consultas do Access, na verdade, são instruções SQL criadas durante a criação de uma consulta com a grade de design na janela Consulta. A tabela a seguir mostra as consultas ação e as consultas de definições de dados, do Access, e as respectivas instruções SQL.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de consulta</p></th>
<th><p>Instrução SQL</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Ação</strong></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Acrescentar</p></td>
<td><p>INSERT INTO</p></td>
</tr>
<tr class="odd">
<td><p>Excluir</p></td>
<td><p>DELETE</p></td>
</tr>
<tr class="even">
<td><p>Criar tabela</p></td>
<td><p>SELECIONE … EM</p></td>
</tr>
<tr class="odd">
<td><p>Atualizar</p></td>
<td><p>UPDATE</p></td>
</tr>
<tr class="even">
<td><p><strong>Definição de dados (específica de SQL)</strong></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Criar uma tabela</p></td>
<td><p>CREATE TABLE</p></td>
</tr>
<tr class="even">
<td><p>Alterar uma tabela</p></td>
<td><p>ALTER TABLE</p></td>
</tr>
<tr class="odd">
<td><p>Excluir uma tabela</p></td>
<td><p>DROP TABLE</p></td>
</tr>
<tr class="even">
<td><p>Criar um índice</p></td>
<td><p>CREATE INDEX</p></td>
</tr>
<tr class="odd">
<td><p>Excluir um índice</p></td>
<td><p>DROP INDEX</p></td>
</tr>
</tbody>
</table>

Você também pode usar uma cláusula IN com essas instruções para modificar dados em outro banco de dados.

> [!NOTE]
> [!OBSERVAçãO] Para executar uma consulta seleção ou uma consulta de tabela de referência cruzada em uma macro, use o argumento Exibir da ação **AbrirConsulta** para abrir uma consulta seleção ou uma consulta de tabela de referência cruzada existente no modo Folha de Dados. Consultas ação e consultas específicas de SQL existentes também podem ser executadas dessa mesma forma.
