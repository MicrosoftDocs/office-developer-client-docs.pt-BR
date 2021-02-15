---
title: Connection.Exemétodo cute (DAO)
TOCTitle: Execute Method
ms:assetid: d6140d4e-fa14-6455-525e-49d8aab3dff7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835040(v=office.15)
ms:contentKeyID: 48547978
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8140dbe9bc0c68d467c011d77bc0c00cec7ad560
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295909"
---
# <a name="connectionexecute-method-dao"></a>Connection.Exemétodo cute (DAO)

**Aplica-se ao**: Access 2013, Office 2013

Executa uma consulta de ação ou executa uma instrução SQL no objeto especificado.

## <a name="syntax"></a>Sintaxe

*expression* .Execute(***Query***, ***Options***)

*expressão* Uma variável que representa um objeto **Connection**.

## <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Necessária/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Query</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Uma <strong>String</strong> que é uma instrução SQL ou o valor da propriedade <strong>Name</strong> de um objeto <strong>QueryDef</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>Opções</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variantes</strong></p></td>
<td><p>Uma constante ou combinação de constantes que determina as características de integridade dos dados da consulta, conforme especificado em Configurações.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode usar as seguintes constantes **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** para options.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbDenyWrite</strong></p></td>
<td><p>Nega a permissão de gravação para outros usuários (somente espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbInconsistent</strong></p></td>
<td><p>(Padrão) Executa atualizações inconsistentes (somente espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbConsistent</strong></p></td>
<td><p>Executa atualizações consistentes (somente espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSQLPassThrough</strong></p></td>
<td><p>Executa uma consulta de passagem SQL. A configuração dessa opção passa a instrução SQL para um banco de dados ODBC para processamento (somente espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFailOnError</strong></p></td>
<td><p>Reverte atualizações se ocorrer erro (somente espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSeeChanges</strong></p></td>
<td><p>Gera um erro de tempo de execução caso outro usuário esteja alterando dados que você esteja editando (somente espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Executa a consulta de forma assíncrona (somente objetos ODBCDirect Connection e QueryDef).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbExecDirect</strong></p></td>
<td><p>Executa a instrução sem chamar primeiro a função SQLPrepare ODBC API (somente objetos ODBCDirect Connection e QueryDef).</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.

> [!NOTE]
> As constantes **dbConsistent** e **dbInconsistent** são mutuamente exclusivas. Você pode usar uma ou outra, as não ambas em uma determinada instância de **OpenRecordset**. Usar **dbConsistent** e **dbInconsistent** causará um erro.

O método **Execute** só será válido para consultas de ação. Se você usar **Execute** com outro tipo de consulta, ocorrerá um erro. Como uma consulta de ação não retorna registros, **Execute** não retorna um **Recordset** (a execução de uma consulta de passagem SQL em um espaço de trabalho ODBCDirect não retornará um erro se um **Recordset** não for retornado).

Use a propriedade **RecordsAffected** do objeto **Connection**, **Database** ou **QueryDef** para determinar o número de registros afetados pelo método **Execute** mais recente. Por exemplo, **RecordsAffected** contém o número de registros excluídos, atualizados ou inseridos na execução de uma consulta de ação. Quando você usar o método **Execute** para executar uma consulta, a propriedade **RecordsAffected** do objeto **QueryDef** é definida como o número de registros afetados.

Em um espaço de trabalho do Microsoft Access, se você fornecer uma instrução SQL sintaticamente correta e tiver as permissões apropriadas, o método **Execute** não falhará  mesmo que uma única linha possa ser modificada ou excluída. Portanto, sempre use a opção **dbFailOnError** quando empregar o método **Execute** para executar uma consulta atualização ou exclusão. Essa opção gera um erro em tempo de execução e devolve todas as alterações bem-sucedidas se qualquer um dos registros afetados estiver protegido e não puder ser atualizado ou excluído.

Em versões anteriores do mecanismo de banco de dados do Microsoft Jet, instruções SQL foram automaticamente incorporadas a transações implícitas. Se parte de uma instrução executada com o **dbFailOnError** tiver falhado, a instrução inteira será devolvida. Para melhorar o desempenho, essas transações implícitas foram removidas a partir da versão 3.5. Se estiver atualizando código DAO antigo, considere o uso de transações explícitas envolvendo instruções **Execute**.

Para obter o melhor desempenho em um espaço de trabalho do Microsoft Access, especialmente em um ambiente multiusuário, aninhe o método **Execute** em uma transação. Use o método **BeginTrans** no objeto **Espaço de Trabalho** atual, então use o método **Execute** e conclua a transação usando o método **CommitTrans** no **Espaço de Trabalho**. Isso salva alterações no disco e libera qualquer bloqueio gerado durante a execução da consulta.

