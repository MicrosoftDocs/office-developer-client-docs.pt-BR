---
title: Método DBEngine.Rollback (DAO)
TOCTitle: Rollback Method
ms:assetid: da7e2fe0-c837-7b1e-d35c-98e6cb0a7bbe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835327(v=office.15)
ms:contentKeyID: 48548084
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053424
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 378baa8cd2923366a453a6cf23d51af0ab0df5ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294201"
---
# <a name="dbenginerollback-method-dao"></a>Método DBEngine.Rollback (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Encerra a transação atual e restaura os bancos de dados no objeto **Workspace** para o estado em que estavam quando a transação atual começou.

## <a name="syntax"></a>Sintaxe

*expressão* . Rollback

*expressão* Uma variável que representa um objeto **DBEngine**.

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

  - Você pode normalmente aumentar o desempenho do aplicativo separar em blocos de transação as operações que exigem acesso ao disco. Isso fornece um buffer para suas operações e pode reduzir significativamente o número de vezes que um disco é acessado.

  - Em um espaço de trabalho do Microsoft Access, as transações são registradas em um arquivo mantido no diretório especificado pela variável de ambiente TEMP na estação de trabalho. Se o arquivo de log da transação esgotar o espaço de repositório disponível na unidade TEMP, o mecanismo de banco de dados acionará um erro em tempo de execução. Nesse momento, se você usar **CommitTrans**, um número indeterminado de operações será confirmado, mas as operações não concluídas restantes serão perdidas e a operação terá que ser reiniciada. A utilização de um método **Rollback** libera o log de transação e reverte todas as operações na transação.

  - Fechar um **Recordset** de clone dentro de uma transação pendente causa uma operação **Rollback** implícita.

