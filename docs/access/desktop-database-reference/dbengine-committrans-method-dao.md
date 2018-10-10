---
title: Método DBEngine.CommitTrans (DAO)
TOCTitle: CommitTrans Method
ms:assetid: 0c9d345f-13ff-7fe6-789d-fbdb43fa54b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845171(v=office.15)
ms:contentKeyID: 48543197
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3306c81af03b374416c948f44107690f188769cc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465198"
---
# <a name="dbenginecommittrans-method-dao"></a><span data-ttu-id="67f1e-102">Método DBEngine.CommitTrans (DAO)</span><span class="sxs-lookup"><span data-stu-id="67f1e-102">DBEngine.CommitTrans Method (DAO)</span></span>


<span data-ttu-id="67f1e-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="67f1e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="67f1e-104">Encerra a transação atual e salva as alterações.</span><span class="sxs-lookup"><span data-stu-id="67f1e-104">Ends the current transaction and saves the changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="67f1e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67f1e-105">Syntax</span></span>

<span data-ttu-id="67f1e-106">*expressão* . CommitTrans (***opção***)</span><span class="sxs-lookup"><span data-stu-id="67f1e-106">*expression* .CommitTrans(***Option***)</span></span>

<span data-ttu-id="67f1e-107">*expressão* Uma variável que representa um objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="67f1e-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="67f1e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67f1e-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67f1e-109">Nome</span><span class="sxs-lookup"><span data-stu-id="67f1e-109">Name</span></span></p></th>
<th><p><span data-ttu-id="67f1e-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="67f1e-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="67f1e-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="67f1e-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="67f1e-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="67f1e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67f1e-113">Opção</span><span class="sxs-lookup"><span data-stu-id="67f1e-113">Option</span></span></p></td>
<td><p><span data-ttu-id="67f1e-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="67f1e-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="67f1e-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="67f1e-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="67f1e-p101">Em um espaço de trabalho do Microsoft Access, você pode incluir a constante <strong>dbForceOSFlush</strong> com <strong>CommitTrans</strong>. Isso força o mecanismo de banco de dados para retirar imediatamente todas as atualizações do disco, em vez de armazená-las em cache temporariamente. Sem utilizar essa opção, um usuário pode obter de volta o controle logo depois de o programa de aplicativo chamar <strong>CommitTrans</strong>, desligar o computador e não ter os dados gravados no disco. Utilizar essa opção pode afetar o desempenho do aplicativo; ela é útil em situações na qual o computador pode ser desligado antes de as atualizações no cache serem salvas no disco.</span><span class="sxs-lookup"><span data-stu-id="67f1e-p101">In a Microsoft Access workspace, you can include the <strong>dbForceOSFlush</strong> constant with <strong>CommitTrans</strong>. This forces the database engine to immediately flush all updates to disk, instead of caching them temporarily. Without using this option, a user could get control back immediately after the application program calls <strong>CommitTrans</strong>, turn the computer off, and not have the data written to disk. While using this option may affect your application's performance, it is useful in situations where the computer could be shut off before cached updates are saved to disk.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="67f1e-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="67f1e-120">Remarks</span></span>

<span data-ttu-id="67f1e-p102">Os métodos de transação **BeginTrans**, **CommitTrans** e **Rollback** gerenciam o processamento da transação durante uma sessão definida por um objeto **Workspace**. Você utiliza esses métodos com o objeto **Workspace** quando quer tratar uma série de alterações feitas nos bancos de dados em uma sessão como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="67f1e-p102">The transaction methods **BeginTrans**, **CommitTrans**, and **Rollback** manage transaction processing during a session defined by a **Workspace** object. You use these methods with a **Workspace** object when you want to treat a series of changes made to the databases in a session as one unit.</span></span>

<span data-ttu-id="67f1e-p103">Normalmente, você usa as transações para manter a integridade dos dados quando precisa atualizar os registros em duas ou mais tabelas e garantir que as alterações estejam concluídas (confirmadas) em todas as tabelas ou em nenhuma (revertidas). Por exemplo, se você transferir dinheiro de uma conta para outra, poderá subtrair o valor de uma e incluí-lo na outra. Se a atualização falhar, as contas não apresentaram mais esse equilíbrio. Use o método **BeginTrans** antes de atualizar o primeiro registro e, em seguida, se qualquer atualização subsequente falhar, use o método **Rollback** para desfazer todas as atualizações. Use o método **CommitTrans** depois de atualizar com sucesso o último registro.</span><span class="sxs-lookup"><span data-stu-id="67f1e-p103">Typically, you use transactions to maintain the integrity of your data when you must both update records in two or more tables and ensure changes are completed (committed) in all tables or none at all (rolled back). For example, if you transfer money from one account to another, you might subtract an amount from one and add the amount to another. If either update fails, the accounts no longer balance. Use the **BeginTrans** method before updating the first record, and then, if any subsequent update fails, you can use the **Rollback** method to undo all of the updates. Use the **CommitTrans** method after you successfully update the last record.</span></span>


> [!NOTE]
> <P><span data-ttu-id="67f1e-p104">[!OBSERVAçãO] Dentro de um objeto <STRONG>Workspace</STRONG>, as transações são sempre globais para o <STRONG>Workspace</STRONG> e não são limitadas a apenas um objeto <STRONG>Connection</STRONG> ou <STRONG>Database</STRONG>. Se você executar as operações em mais de uma conexão ou banco de dados dentro de uma transação <STRONG>Workspace</STRONG>, resolver a transação (isto é, utilizar os métodos <STRONG>CommitTrans</STRONG> ou <STRONG>Rollback</STRONG>) afetará todas as operações em todas as conexões e bancos de dados dentro daquele espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="67f1e-p104">Within one <STRONG>Workspace</STRONG> object, transactions are always global to the <STRONG>Workspace</STRONG> and aren't limited to only one <STRONG>Connection</STRONG> or <STRONG>Database</STRONG> object. If you perform operations on more than one connection or database within a <STRONG>Workspace</STRONG> transaction, resolving the transaction (that is, using the <STRONG>CommitTrans</STRONG> or <STRONG>Rollback</STRONG> method) affects all operations on all connections and databases within that workspace.</span></span></P>



<span data-ttu-id="67f1e-p105">Depois de usar **CommitTrans**, não é possível desfazer as alterações feitas durante a transação a menos que a transação esteja aninhada dentro de outra transação que foi revertida. Se você aninhar transações, deverá resolver a transação atual antes de resolver uma transação em um nível superior de aninhamento.</span><span class="sxs-lookup"><span data-stu-id="67f1e-p105">After you use **CommitTrans**, you can't undo changes made during that transaction unless the transaction is nested within another transaction that is itself rolled back. If you nest transactions, you must resolve the current transaction before you can resolve a transaction at a higher level of nesting.</span></span>

<span data-ttu-id="67f1e-132">Se você quiser ter transações simultâneas com sobreposição e escopos não aninhados, poderá criar objetos **Workspace** adicionais para conter as transações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="67f1e-132">If you want to have simultaneous transactions with overlapping, non-nested scopes, you can create additional **Workspace** objects to contain the concurrent transactions.</span></span>

<span data-ttu-id="67f1e-133">Se você fechar um objeto **Workspace** sem resolver nenhuma transação pendente, as transações serão automaticamente revertidas.</span><span class="sxs-lookup"><span data-stu-id="67f1e-133">If you close a **Workspace** object without resolving any pending transactions, the transactions are automatically rolled back.</span></span>

<span data-ttu-id="67f1e-134">Se você usar o método **CommitTrans** ou **Rollback** sem primeiro utilizar o método **BeginTrans**, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="67f1e-134">If you use the **CommitTrans** or **Rollback** method without first using the **BeginTrans** method, an error occurs.</span></span>

<span data-ttu-id="67f1e-p106">Alguns banco de dados ISAM utilizados em um espaço de trabalho do Microsoft Access podem não aceitar transações, caso em que a propriedade **Transactions** do objeto **Database** ou **Recordset** é **False**. Para certificar-se de que o banco de dados aceita transações, verifique o valor da propriedade **Transactions** do objeto **Database** antes de utilizar o método **BeginTrans**. Se você estiver utilizando um objeto **Recordset** com base em mais de um banco de dados, verifique a propriedade **Transactions** do objeto **Recordset**. Se **Recordset** basear-se inteiramente nas tabelas do mecanismo de banco de dados do Microsoft Access, você poderá sempre utilizar as transações. Os objetos **Recordset** com base nas tabelas criadas por outros produtos de banco de dados, no entanto, podem não aceitar transações. Por exemplo, não é possível usar transações em um **Recordset** que se baseia em uma tabela Paradox. Nesse caso, a propriedade **Transactions** é **False**. Se **Database** ou **Recordset** não aceitar transações, os métodos serão ignorados e não ocorrerá nenhum erro.</span><span class="sxs-lookup"><span data-stu-id="67f1e-p106">Some ISAM databases used in a Microsoft Access workspace may not support transactions, in which case the **Transactions** property of the **Database** object or **Recordset** object is **False**. To make sure the database supports transactions, check the value of the **Transactions** property of the **Database** object before using the **BeginTrans** method. If you are using a **Recordset** object based on more than one database, check the **Transactions** property of the **Recordset** object. If a **Recordset** is based entirely on Microsoft Access database engine tables, you can always use transactions. **Recordset** objects based on tables created by other database products, however, may not support transactions. For example, you can't use transactions in a **Recordset** based on a Paradox table. In this case, the **Transactions** property is **False**. If the **Database** or **Recordset** doesn't support transactions, the methods are ignored and no error occurs.</span></span>

<span data-ttu-id="67f1e-143">Não será possível aninhar transações se você estiver acessando fontes de dados ODBC pelo mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="67f1e-143">You can't nest transactions if you are accessing ODBC data sources through the Microsoft Access database engine.</span></span>

<span data-ttu-id="67f1e-p107">Nos espaços de trabalho ODBC, quando você usa **CommitTrans**, seu cursor pode não ser mais válido. Use o método **Requery** para exibir as alterações no **Recordset** ou fechar e reabrir o **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="67f1e-p107">In ODBC workspaces, when you use **CommitTrans** your cursor may no longer be valid. Use the **Requery** method to view the changes in the **Recordset**, or close and re-open the **Recordset**.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="67f1e-p108">Você pode normalmente aumentar o desempenho do aplicativo separar em blocos de transação as operações que exigem acesso ao disco. Isso fornece um buffer para suas operações e pode reduzir significativamente o número de vezes que um disco é acessado.</span><span class="sxs-lookup"><span data-stu-id="67f1e-p108">You can often improve the performance of your application by breaking operations that require disk access into transaction blocks. This buffers your operations and may significantly reduce the number of times a disk is accessed.</span></span></P>
> <LI>
> <P><span data-ttu-id="67f1e-p109">Em um espaço de trabalho do Microsoft Access, as transações são registradas em um arquivo mantido no diretório especificado pela variável de ambiente TEMP na estação de trabalho. Se o arquivo de log da transação esgotar o espaço de repositório disponível na unidade TEMP, o mecanismo de banco de dados acionará um erro em tempo de execução. Nesse momento, se você usar <STRONG>CommitTrans</STRONG>, um número indeterminado de operações será confirmado, mas as operações não concluídas restantes serão perdidas e a operação terá que ser reiniciada. A utilização de um método <STRONG>Rollback</STRONG> libera o log de transação e reverte todas as operações na transação.</span><span class="sxs-lookup"><span data-stu-id="67f1e-p109">In a Microsoft Access workspace, transactions are logged in a file kept in the directory specified by the TEMP environment variable on the workstation. If the transaction log file exhausts the available storage on your TEMP drive, the database engine triggers a run-time error. At this point, if you use <STRONG>CommitTrans</STRONG>, an indeterminate number of operations are committed, but the remaining uncompleted operations are lost, and the operation has to be restarted. Using a <STRONG>Rollback</STRONG> method releases the transaction log and rolls back all operations in the transaction.</span></span></P>
> <LI>
> <P><span data-ttu-id="67f1e-152">Fechar um <STRONG>Recordset</STRONG> de clone dentro de uma transação pendente causa uma operação <STRONG>Rollback</STRONG> implícita.</span><span class="sxs-lookup"><span data-stu-id="67f1e-152">Closing a clone <STRONG>Recordset</STRONG> within a pending transaction will cause an implicit <STRONG>Rollback</STRONG> operation.</span></span></P></LI></UL>


