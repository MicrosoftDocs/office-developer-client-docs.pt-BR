---
title: Método DBEngine.CommitTrans (DAO)
TOCTitle: CommitTrans Method
ms:assetid: 0c9d345f-13ff-7fe6-789d-fbdb43fa54b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845171(v=office.15)
ms:contentKeyID: 48543197
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 75918ac4da32020214d9e58d866c5def169eede3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712852"
---
# <a name="dbenginecommittrans-method-dao"></a>Método DBEngine.CommitTrans (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Encerra a transação atual e salva as alterações.

## <a name="syntax"></a>Sintaxe

*expressão* . CommitTrans (***opção***)

*expressão* Uma variável que representa um objeto **DBEngine** .

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
<th><p>Obrigatório/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Option</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Em um espaço de trabalho do Microsoft Access, você pode incluir a constante <strong>dbForceOSFlush</strong> com <strong>CommitTrans</strong>. Isso força o mecanismo de banco de dados para retirar imediatamente todas as atualizações do disco, em vez de armazená-las em cache temporariamente. Sem utilizar essa opção, um usuário pode obter de volta o controle logo depois de o programa de aplicativo chamar <strong>CommitTrans</strong>, desligar o computador e não ter os dados gravados no disco. Utilizar essa opção pode afetar o desempenho do aplicativo; ela é útil em situações na qual o computador pode ser desligado antes de as atualizações no cache serem salvas no disco.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Os métodos de transação **BeginTrans**, **CommitTrans** e **Rollback** gerenciam o processamento da transação durante uma sessão definida por um objeto **Workspace**. Você utiliza esses métodos com o objeto **Workspace** quando quer tratar uma série de alterações feitas nos bancos de dados em uma sessão como uma unidade.

Normalmente, você usa as transações para manter a integridade dos dados quando precisa atualizar os registros em duas ou mais tabelas e garantir que as alterações estejam concluídas (confirmadas) em todas as tabelas ou em nenhuma (revertidas). Por exemplo, se você transferir dinheiro de uma conta para outra, poderá subtrair o valor de uma e incluí-lo na outra. Se a atualização falhar, as contas não apresentaram mais esse equilíbrio. Use o método **BeginTrans** antes de atualizar o primeiro registro e, em seguida, se qualquer atualização subsequente falhar, use o método **Rollback** para desfazer todas as atualizações. Use o método **CommitTrans** depois de atualizar com sucesso o último registro.

> [!NOTE]
> [!OBSERVAçãO] Dentro de um objeto **Workspace**, as transações são sempre globais para o **Workspace** e não são limitadas a apenas um objeto **Connection** ou **Database**. Se você executar as operações em mais de uma conexão ou banco de dados dentro de uma transação **Workspace**, resolver a transação (isto é, utilizar os métodos **CommitTrans** ou **Rollback**) afetará todas as operações em todas as conexões e bancos de dados dentro daquele espaço de trabalho.

Depois de usar **CommitTrans**, não é possível desfazer as alterações feitas durante a transação a menos que a transação esteja aninhada dentro de outra transação que foi revertida. Se você aninhar transações, deverá resolver a transação atual antes de resolver uma transação em um nível superior de aninhamento.

Se você quiser ter transações simultâneas com sobreposição e escopos não aninhados, poderá criar objetos **Workspace** adicionais para conter as transações simultâneas.

Se você fechar um objeto **Workspace** sem resolver nenhuma transação pendente, as transações serão automaticamente revertidas.

Se você usar o método **CommitTrans** ou **Rollback** sem primeiro utilizar o método **BeginTrans**, ocorrerá um erro.

Alguns banco de dados ISAM utilizados em um espaço de trabalho do Microsoft Access podem não aceitar transações, caso em que a propriedade **Transactions** do objeto **Database** ou **Recordset** é **False**. Para certificar-se de que o banco de dados aceita transações, verifique o valor da propriedade **Transactions** do objeto **Database** antes de utilizar o método **BeginTrans**. Se você estiver utilizando um objeto **Recordset** com base em mais de um banco de dados, verifique a propriedade **Transactions** do objeto **Recordset**. Se **Recordset** basear-se inteiramente nas tabelas do mecanismo de banco de dados do Microsoft Access, você poderá sempre utilizar as transações. Os objetos **Recordset** com base nas tabelas criadas por outros produtos de banco de dados, no entanto, podem não aceitar transações. Por exemplo, não é possível usar transações em um **Recordset** que se baseia em uma tabela Paradox. Nesse caso, a propriedade **Transactions** é **False**. Se **Database** ou **Recordset** não aceitar transações, os métodos serão ignorados e não ocorrerá nenhum erro.

Não será possível aninhar transações se você estiver acessando fontes de dados ODBC pelo mecanismo de banco de dados do Microsoft Access.

Nos espaços de trabalho ODBC, quando você usa **CommitTrans**, seu cursor pode não ser mais válido. Use o método **Requery** para exibir as alterações no **Recordset** ou fechar e reabrir o **Recordset**.


> [!NOTE]
> - Você pode normalmente aumentar o desempenho do aplicativo separar em blocos de transação as operações que exigem acesso ao disco. Isso fornece um buffer para suas operações e pode reduzir significativamente o número de vezes que um disco é acessado.
> - Em um espaço de trabalho do Microsoft Access, as transações são registradas em um arquivo mantido no diretório especificado pela variável de ambiente TEMP na estação de trabalho. Se o arquivo de log da transação esgotar o espaço de repositório disponível na unidade TEMP, o mecanismo de banco de dados acionará um erro em tempo de execução. Nesse momento, se você usar **CommitTrans**, um número indeterminado de operações será confirmado, mas as operações não concluídas restantes serão perdidas e a operação terá que ser reiniciada. A utilização de um método **Rollback** libera o log de transação e reverte todas as operações na transação.
> - Fechar um **Recordset** de clone dentro de uma transação pendente causa uma operação **Rollback** implícita.


