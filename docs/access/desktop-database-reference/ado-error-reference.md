---
title: Referência de Erros do ADO
TOCTitle: ADO Error Reference
ms:assetid: 21cec161-664a-4c18-4458-8117f4f63845
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248997(v=office.15)
ms:contentKeyID: 48543690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 53dfb03616b0610ed580f4e576f4c48ef3be8525
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464905"
---
# <a name="ado-error-reference"></a><span data-ttu-id="8054b-102">Referência de Erros do ADO</span><span class="sxs-lookup"><span data-stu-id="8054b-102">ADO Error Reference</span></span>


<span data-ttu-id="8054b-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8054b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8054b-p101">A constante **ErrorValueEnum** descreve os valores de erro do ADO. Para obter uma listagem completa dessas constantes enumeradas, incluindo os valores, consulte [Apêndice B: erros do ADO](appendix-b-ado-errors.md). Esta seção examinará alguns dos erros mais interessantes e explicará algumas situações específicas que podem provocá-los, ou então as soluções para corrigir o problema. São listados a constante **ErrorValueEnum** e o número decimal positivo curto.</span><span class="sxs-lookup"><span data-stu-id="8054b-p101">The **ErrorValueEnum** constant describes the ADO error values. For a complete listing of these enumerated constants, including values, see [Appendix B: ADO Errors](appendix-b-ado-errors.md). This section will examine some of the more interesting errors and explain some specific situations that can raise them, or solutions to fix the problem. Both the **ErrorValueEnum** constant and the short positive decimal number are listed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8054b-108">Número</span><span class="sxs-lookup"><span data-stu-id="8054b-108">Number</span></span></p></th>
<th><p><span data-ttu-id="8054b-109">Constante ErrorValueEnum</span><span class="sxs-lookup"><span data-stu-id="8054b-109">ErrorValueEnum constant</span></span></p></th>
<th><p><span data-ttu-id="8054b-110">Descrição/causas possíveis</span><span class="sxs-lookup"><span data-stu-id="8054b-110">Description/Possible causes</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8054b-111"><strong>3000</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-111"><strong>3000</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-112"><strong>adErrProviderFailed</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-112"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-113">O provedor falhou em executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="8054b-113">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-114"><strong>3001</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-114"><strong>3001</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-115"><strong>adErrInvalidArgument</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-115"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p102">Os argumentos são do tipo incorreto, estão fora do intervalo aceitável ou há conflito entre eles. Este erro frequentemente é causado por um erro ortográfico em uma instrução SELECT do SQL. Por exemplo, um nome de campo ou de tabela incorreto. Este erro também pode ocorrer quando um campo ou uma tabela nomeada em uma instrução SELECT não existe no repositório de dados.</span><span class="sxs-lookup"><span data-stu-id="8054b-p102">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another. This error is often caused by a typographical error in an SQL SELECT statement. For example, a misspelled field name or table name can generate this error. This error can also occur when a field or table named in a SELECT statement does not exist in the data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-120"><strong>3002</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-120"><strong>3002</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-121"><strong>adErrOpeningFile</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-121"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p103">Não foi possível abrir o arquivo. Foi especificado um nome de arquivo incorreto, ou um arquivo foi movido, renomeado ou excluído. Em uma rede, a unidade pode estar temporariamente indisponível ou o tráfego da rede pode estar impedindo uma conexão.</span><span class="sxs-lookup"><span data-stu-id="8054b-p103">File could not be opened. A misspelled file name was specified, or a file has been moved, renamed, or deleted. Over a network, the drive might be temporarily unavailable or network traffic might be preventing a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-125"><strong>3003</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-125"><strong>3003</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-126"><strong>adErrReadFile</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-126"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p104">Não foi possível ler o arquivo. O nome do arquivo está especificado incorretamente, o arquivo pode ter sido movido ou excluído, ou o arquivo pode ter sido corrompido.</span><span class="sxs-lookup"><span data-stu-id="8054b-p104">File could not be read. The name of the file is specified incorrectly, the file might have been moved or deleted, or the file might have become corrupted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-129"><strong>3004</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-129"><strong>3004</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-130"><strong>adErrWriteFile</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-130"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p105">Falha ao gravar no arquivo. Talvez você tenha fechado um arquivo e, em seguida, tentado gravar nele, ou o arquivo pode estar corrompido. Se o arquivo estiver localizado em uma unidade de rede, as condições transitórias da rede podem impedir a gravação em uma unidade de rede.</span><span class="sxs-lookup"><span data-stu-id="8054b-p105">Write to file failed. You might have closed a file and then tried to write to it, or the file might be corrupted. If the file is located on a network drive, transient network conditions might prevent writing to a network drive.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-134"><strong>3021</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-134"><strong>3021</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-135"><strong>adErrNoCurrentRecord</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-135"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-136"><strong>BOF</strong> ou <strong>EOF</strong> for True, ou o registro atual foi excluído.</span><span class="sxs-lookup"><span data-stu-id="8054b-136">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted.</span></span> <span data-ttu-id="8054b-137">Operação solicitada requer um registro atual.</span><span class="sxs-lookup"><span data-stu-id="8054b-137">Requested operation requires a current record.</span></span> <span data-ttu-id="8054b-138">Foi feita uma tentativa para atualizar registros usando <strong>Localizar</strong> ou <strong>Seek</strong> para mover o ponteiro do registro para o registro desejado.</span><span class="sxs-lookup"><span data-stu-id="8054b-138">An attempt was made to update records by using <strong>Find</strong> or <strong>Seek</strong> to move the record pointer to the desired record.</span></span> <span data-ttu-id="8054b-139">Se o registro não for encontrado, <strong>EOF</strong> serão True.</span><span class="sxs-lookup"><span data-stu-id="8054b-139">If the record is not found, <strong>EOF</strong> will be True.</span></span> <span data-ttu-id="8054b-140">Esse erro também pode ocorrer após uma <strong>AddNew</strong> com falha ou <strong>Excluir</strong> porque não há nenhum registro atual quando esses métodos falham.</span><span class="sxs-lookup"><span data-stu-id="8054b-140">This error can also occur after a failed <strong>AddNew</strong> or <strong>Delete</strong> because there is no current record when these methods fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-141"><strong>3219</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-141"><strong>3219</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-142"><strong>adErrIllegalOperation</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-142"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-143">A operação não é permitida nesse contexto.</span><span class="sxs-lookup"><span data-stu-id="8054b-143">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-144"><strong>3220</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-144"><strong>3220</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-145"><strong>adErrCantChangeProvider</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-145"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-146">O provedor designado é diferente daquele que está em uso.</span><span class="sxs-lookup"><span data-stu-id="8054b-146">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-147"><strong>3246</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-147"><strong>3246</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-148"><strong>adErrInTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-148"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p107">O objeto <strong>Connection</strong> não pode ser fechado explicitamente durante uma transação. Um objeto <strong>Recordset</strong> ou <strong>Connection</strong> que está participando de uma transação no momento não pode ser fechado. Chame <strong>RollbackTrans</strong> ou <strong>CommitTrans</strong> antes de fechar o objeto.</span><span class="sxs-lookup"><span data-stu-id="8054b-p107"><strong>Connection</strong> object cannot be explicitly closed while in a transaction. A <strong>Recordset</strong> or <strong>Connection</strong> object that is currently participating in a transaction cannot be closed. Call either <strong>RollbackTrans</strong> or <strong>CommitTrans</strong> before closing the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-152"><strong>3251</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-152"><strong>3251</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-153"><strong>adErrFeatureNotAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-153"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p108">O objeto ou provedor não consegue executar a operação solicitada. Algumas operações dependem de uma determinada versão do provedor.</span><span class="sxs-lookup"><span data-stu-id="8054b-p108">The object or provider is not capable of performing the requested operation. Some operations depend on a particular provider version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-156"><strong>3265</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-156"><strong>3265</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-157"><strong>adErrItemNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-157"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p109">O item não foi encontrado na coleção correspondente ao nome ou ordinal solicitado. Foi especificado um nome de campo ou de tabela incorreto.</span><span class="sxs-lookup"><span data-stu-id="8054b-p109">Item cannot be found in the collection corresponding to the requested name or ordinal. An incorrect field or table name has been specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-160"><strong>3367</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-160"><strong>3367</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-161"><strong>adErrObjectInCollection</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-161"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p110">O objeto já está na coleção e não pode ser anexado. Não é possível adicionar um objeto à mesma coleção duas vezes.</span><span class="sxs-lookup"><span data-stu-id="8054b-p110">Object is already in collection. Cannot append. An object cannot be added to the same collection twice.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-165"><strong>3420</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-165"><strong>3420</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-166"><strong>adErrObjectNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-166"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-167">O objeto não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="8054b-167">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-168"><strong>3421</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-168"><strong>3421</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-169"><strong>adErrDataConversion</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-169"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p111">O aplicativo usa um valor do tipo incorreto para a operação atual. Talvez você tenha fornecido uma sequência de caracteres para uma operação que espera um fluxo, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="8054b-p111">Application uses a value of the wrong type for the current operation. You might have supplied a string to an operation that expects a stream, for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-172"><strong>3704</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-172"><strong>3704</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-173"><strong>adErrObjectClosed</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-173"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p112">A operação não é permitida quando o objeto está fechado. O objeto <strong>Connection</strong> ou <strong>Recordset</strong> foi fechado. Por exemplo, alguma outra rotina pode ter fechado um objeto global. Este erro pode ser evitado com a verificação da propriedade <strong>State</strong> antes de tentar uma operação.</span><span class="sxs-lookup"><span data-stu-id="8054b-p112">Operation is not allowed when the object is closed. The <strong>Connection</strong> or <strong>Recordset</strong> has been closed. For example, some other routine might have closed a global object. You can prevent this error by checking the <strong>State</strong> property before you attempt an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-178"><strong>3705</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-178"><strong>3705</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-179"><strong>adErrObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-179"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p113">A operação não é permitida quando o objeto está aberto. Um objeto aberto não pode estar aberto. Os campos não podem ser anexados a um <strong>Recordset</strong> aberto.</span><span class="sxs-lookup"><span data-stu-id="8054b-p113">Operation is not allowed when the object is open. An object that is open cannot be opened. Fields cannot be appended to an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-183"><strong>3706</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-183"><strong>3706</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-184"><strong>adErrProviderNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-184"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-185">Provedor não pode ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="8054b-185">Provider cannot be found.</span></span> <span data-ttu-id="8054b-186">Ele pode não ser instalado corretamente.</span><span class="sxs-lookup"><span data-stu-id="8054b-186">It may not be properly installed.</span></span> <span data-ttu-id="8054b-187">O nome do provedor pode estar especificado incorretamente, o provedor especificado talvez não esteja instalado no computador em que o código está sendo executado, ou a instalação pode ter sido corrompida.</span><span class="sxs-lookup"><span data-stu-id="8054b-187">The name of the provider might be incorrectly specified, the specified provider might not be installed on the computer where your code is being executed, or the installation might have become corrupted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-188"><strong>3707</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-188"><strong>3707</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-189"><strong>adErrBoundToCommand</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-189"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p115">A propriedade <strong>ActiveConnection</strong> de um objeto <strong>Recordset</strong>, que tem um objeto <strong>Command</strong> como fonte, não pode ser alterada. O aplicativo tentou atribuir um novo objeto <strong>Connection</strong> a um <strong>Recordset</strong> cuja fonte é um objeto <strong>Command</strong>.</span><span class="sxs-lookup"><span data-stu-id="8054b-p115">The <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object, which has a <strong>Command</strong> object as its source, cannot be changed. The application attempted to assign a new <strong>Connection</strong> object to a <strong>Recordset</strong> that has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-192"><strong>3708</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-192"><strong>3708</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-193"><strong>adErrInvalidParamInfo</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-193"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p116">O objeto <strong>Parameter</strong> é definido de forma incorreta. Foram fornecidas informações inconsistentes ou incompletas.</span><span class="sxs-lookup"><span data-stu-id="8054b-p116"><strong>Parameter</strong> object is improperly defined. Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-196"><strong>3709</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-196"><strong>3709</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-197"><strong>adErrInvalidConnection</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-197"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p117">A conexão não pode ser usada para executar essa operação. Ela está fechada ou é inválida nesse contexto.</span><span class="sxs-lookup"><span data-stu-id="8054b-p117">The connection cannot be used to perform this operation. It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-200"><strong>3710</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-200"><strong>3710</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-201"><strong>adErrNotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-201"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p118">A operação não pode ser executada durante o processamento do evento. Uma operação não pode ser executada em um manipulador de eventos que faz com que o evento seja acionado novamente. Por exemplo, os métodos de navegação não devem ser chamados a partir de um manipulador de eventos <strong>WillMove</strong>.</span><span class="sxs-lookup"><span data-stu-id="8054b-p118">Operation cannot be performed while processing event. An operation cannot be performed within an event handler that causes the event to fire again. For example, navigation methods should not be called from within a <strong>WillMove</strong> event handler.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-205"><strong>3711</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-205"><strong>3711</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-206"><strong>adErrStillExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-206"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-207">A operação não pode ser executada durante uma execução assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8054b-207">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-208"><strong>3712</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-208"><strong>3712</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-209"><strong>adErrOperationCancelled</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-209"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p119">A operação foi cancelada pelo usuário. O aplicativo chamou o método <strong>CancelUpdate</strong> ou <strong>CancelBatch</strong> e a operação atual foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="8054b-p119">Operation has been canceled by the user. The application has called the <strong>CancelUpdate</strong> or <strong>CancelBatch</strong> method and the current operation has been canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-212"><strong>3713</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-212"><strong>3713</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-213"><strong>adErrStillConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-213"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-214">A operação não pode ser executada durante a conexão assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8054b-214">Operation cannot be performed while connecting asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-215"><strong>3714</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-215"><strong>3714</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-216"><strong>adErrInvalidTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-216"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-217">A transação de coordenação é inválida ou não foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="8054b-217">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-218"><strong>3715</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-218"><strong>3715</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-219"><strong>adErrNotExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-219"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-220">A operação não pode ser executada sozinha.</span><span class="sxs-lookup"><span data-stu-id="8054b-220">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-221"><strong>3716</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-221"><strong>3716</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-222"><strong>adErrUnsafeOperation</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-222"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-223">As configurações de segurança nesse computador proíbem o acesso à fonte de dados em outro domínio.</span><span class="sxs-lookup"><span data-stu-id="8054b-223">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-224"><strong>3717</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-224"><strong>3717</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-225"><strong>adWrnSecurityDialog</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-225"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p120">Somente para uso interno. Não use. (Entrada incluída para fins de complementação. Este erro não deve aparecer no seu código.)</span><span class="sxs-lookup"><span data-stu-id="8054b-p120">For internal use only. Don't use. (Entry was included for the sake of completeness. This error should not appear in your code.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-230"><strong>3718</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-230"><strong>3718</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-231"><strong>adWrnSecurityDialogHeader</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-231"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p121">Somente para uso interno. Não use. (Entrada incluída para fins de complementação. Este erro não deve aparecer no seu código.)</span><span class="sxs-lookup"><span data-stu-id="8054b-p121">For internal use only. Don't use. (Entry included for the sake of completeness. This error should not appear in your code.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-236"><strong>3719</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-236"><strong>3719</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-237"><strong>adErrIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-237"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p122">Conflito entre valores de dados e as restrições de integridade do campo. Um novo valor para um <strong>Campo</strong> causaria uma chave duplicada. Um valor que forma um lado de uma relação entre dois registros pode não ser atualizável.</span><span class="sxs-lookup"><span data-stu-id="8054b-p122">Data value conflicts with the integrity constraints of the field. A new value for a <strong>Field</strong> would cause a duplicate key. A value that forms one side of a relationship between two records might not be updatable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-241"><strong>3720</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-241"><strong>3720</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-242"><strong>adErrPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-242"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p123">A permissão insuficiente impede a gravação no campo. O usuário nomeado na sequência de conexão não tem as permissões adequadas para gravar em um <strong>Campo</strong>.</span><span class="sxs-lookup"><span data-stu-id="8054b-p123">Insufficient permission prevents writing to the field. The user named in the connection string does not have the proper permissions to write to a <strong>Field</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-245"><strong>3721</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-245"><strong>3721</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-246"><strong>adErrDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-246"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p124">O valor dos dados é muito grande para ser representado pelo tipo de dados do campo. Foi atribuído um valor numérico muito grande para o campo a que se destina. Por exemplo, um valor inteiro longo foi atribuído a um campo de inteiro curto.</span><span class="sxs-lookup"><span data-stu-id="8054b-p124">Data value is too large to be represented by the field data type. A numeric value that is too large for the intended field was assigned. For example, a long integer value was assigned to a short integer field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-250"><strong>3722</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-250"><strong>3722</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-251"><strong>adErrSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-251"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p125">Conflito entre valores de dados e o tipo de dados ou as restrições do campo. O repositório de dados possui restrições de validação diferentes do valor do <strong>Campo</strong>.</span><span class="sxs-lookup"><span data-stu-id="8054b-p125">Data value conflicts with the data type or constraints of the field. The data store has validation constraints that differ from the <strong>Field</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-254"><strong>3723</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-254"><strong>3723</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-255"><strong>adErrSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-255"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-256">A conversão falhou porque o valor dos dados era assinado e o tipo de dados do campo utilizado pelo provedor não era.</span><span class="sxs-lookup"><span data-stu-id="8054b-256">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-257"><strong>3724</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-257"><strong>3724</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-258"><strong>adErrCantConvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-258"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p126">O valor dos dados não pode ser convertido por razões diferentes de incompatibilidade assinada ou estouro de dados. Por exemplo, a conversão truncaria os dados.</span><span class="sxs-lookup"><span data-stu-id="8054b-p126">Data value cannot be converted for reasons other than sign mismatch or data overflow. For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-261"><strong>3725</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-261"><strong>3725</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-262"><strong>adErrCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-262"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-263">O valor dos dados não pode ser definido ou recuperado porque o tipo de dados do campo é desconhecido ou o provedor tem recursos insuficientes para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="8054b-263">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-264"><strong>3726</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-264"><strong>3726</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-265"><strong>adErrColumnNotOnThisRow</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-265"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p127">O registro não contém esse campo. Foi especificado um nome de campo incorreto ou um campo que não está na coleção <strong>Fields</strong> do registro atual foi referenciado.</span><span class="sxs-lookup"><span data-stu-id="8054b-p127">Record does not contain this field. An incorrect field name was specified or a field not in the <strong>Fields</strong> collection of the current record was referenced.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-268"><strong>3727</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-268"><strong>3727</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-269"><strong>adErrURLDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-269"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-270">A URL de origem ou o pai da URL de destino não existe.</span><span class="sxs-lookup"><span data-stu-id="8054b-270">Either the source URL or the parent of the destination URL does not exist.</span></span> <span data-ttu-id="8054b-271">Há um erro de digitação na URL de origem ou de destino.</span><span class="sxs-lookup"><span data-stu-id="8054b-271">There is a typographical error in either the source or destination URL.</span></span> <span data-ttu-id="8054b-272">Você pode ter https://mysite/photo/myphoto.jpg quando você na realidade deveria ter https://mysite/photos/myphoto.jpg em vez disso.</span><span class="sxs-lookup"><span data-stu-id="8054b-272">You might have https://mysite/photo/myphoto.jpg when you should actually have https://mysite/photos/myphoto.jpg instead.</span></span> <span data-ttu-id="8054b-273">O erro de digitação na URL pai (no caso, a <em>foto</em> em vez de <em>fotos</em>) causou o erro.</span><span class="sxs-lookup"><span data-stu-id="8054b-273">The typographical error in the parent URL (in this case, <em>photo</em> instead of <em>photos</em>) has caused the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-274"><strong>3728</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-274"><strong>3728</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-275"><strong>adErrTreePermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-275"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p129">As permissões são insuficientes para acessar a árvore ou subárvore. O usuário nomeado na sequência de conexão não tem as permissões adequadas.</span><span class="sxs-lookup"><span data-stu-id="8054b-p129">Permissions are insufficient to access tree or subtree. The user named in the connection string does not have the appropriate permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-278"><strong>3729</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-278"><strong>3729</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-279"><strong>adErrInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-279"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p130">A URL contém caracteres inválidos. Verifique se ela está digitada corretamente. A URL segue o esquema registrado para o provedor atual (por exemplo, Internet Publishing Provider está registrado para http).</span><span class="sxs-lookup"><span data-stu-id="8054b-p130">URL contains invalid characters. Make sure the URL is typed correctly. The URL follows the scheme registered to the current provider (for example, Internet Publishing Provider is registered for http).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-283"><strong>3730</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-283"><strong>3730</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-284"><strong>adErrResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-284"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p131">O objeto representado pela URL especificada está bloqueado por um ou mais processos. Aguarde a conclusão do processo e tente a operação novamente. O objeto que você está tentando acessar foi bloqueado por outro usuário ou por outro processo no seu aplicativo. É mais provável que isso aconteça em um ambiente multiusuário.</span><span class="sxs-lookup"><span data-stu-id="8054b-p131">Object represented by the specified URL is locked by one or more other processes. Wait until the process has finished and attempt the operation again. The object you are trying to access has been locked by another user or by another process in your application. This is most likely to arise in a multi-user environment.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-289"><strong>3731</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-289"><strong>3731</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-290"><strong>adErrResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-290"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p132">A operação de cópia não pode ser executada. O objeto nomeado pela URL de destino já existe. Especifique <strong>adCopyOverwrite</strong> para substituí-lo. Se você não especificar <strong>adCopyOverwrite</strong> ao copiar os arquivos em um diretório, haverá falha quando você tentar copiar um item que já existe no local de destino.</span><span class="sxs-lookup"><span data-stu-id="8054b-p132">Copy operation cannot be performed. Object named by destination URL already exists. Specify <strong>adCopyOverwrite</strong> to replace the object. If you do not specify <strong>adCopyOverwrite</strong> when copying the files in a directory, the copy fails when you try to copy an item that already exists in the destination location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-295"><strong>3732</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-295"><strong>3732</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-296"><strong>adErrCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-296"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p133">O servidor não pode concluir a operação. Isso pode ocorrer porque o servidor está ocupado com outras operações ou porque os recursos do servidor são insuficientes.</span><span class="sxs-lookup"><span data-stu-id="8054b-p133">The server cannot complete the operation. This might be because the server is busy with other operations or it might be low on resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-299"><strong>3733</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-299"><strong>3733</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-300"><strong>adErrVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-300"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p134">O provedor não pode localizar o dispositivo de repositório indicado pela URL. Verifique se a URL está digitada corretamente. A URL do dispositivo de repositório pode estar incorreta, mas este erro pode ocorrer por outros motivos. É possível que o dispositivo esteja offline ou um grande volume de tráfego da rede pode impedir que a conexão seja estabelecida.</span><span class="sxs-lookup"><span data-stu-id="8054b-p134">Provider cannot locate the storage device indicated by the URL. Make sure the URL is typed correctly. The URL of the storage device might be incorrect, but this error can occur for other reasons. The device might be offline or a large volume of network traffic might prevent the connection from being made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-305"><strong>3734</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-305"><strong>3734</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-306"><strong>adErrOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-306"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p135">A operação não pode ser executada. O provedor não pode obter espaço de repositório suficiente. Talvez não haja RAM ou espaço no disco rígido suficiente para os arquivos temporários no servidor.</span><span class="sxs-lookup"><span data-stu-id="8054b-p135">Operation cannot be performed. Provider cannot obtain enough storage space. There might not be enough RAM or hard-drive space for temporary files on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-310"><strong>3735</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-310"><strong>3735</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-311"><strong>adErrResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-311"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-312">A URL de origem ou de destino está fora do escopo do registro atual.</span><span class="sxs-lookup"><span data-stu-id="8054b-312">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-313"><strong>3736</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-313"><strong>3736</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-314"><strong>adErrUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-314"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p136">A operação não pôde ser concluída e o status não está disponível. O campo pode estar indisponível ou a operação não foi tentada. Outro usuário pode ter alterado ou excluído o campo que você está tentando acessar.</span><span class="sxs-lookup"><span data-stu-id="8054b-p136">Operation failed to complete and the status is unavailable. The field may be unavailable or the operation was not attempted. Another user might have changed or deleted the field you are trying to access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-318"><strong>3737</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-318"><strong>3737</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-319"><strong>adErrURLNamedRowDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-319"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p137">O registro nomeado por essa URL não existe. Durante a tentativa de abrir um arquivo usando um objeto <strong>Record</strong>, o nome do arquivo ou o caminho para o arquivo estava incorreto.</span><span class="sxs-lookup"><span data-stu-id="8054b-p137">Record named by this URL does not exist. While attempting to open a file using a <strong>Record</strong> object, either the file name or the path to the file was misspelled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-322"><strong>3738</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-322"><strong>3738</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-323"><strong>adErrDelResOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-323"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-324">A URL do objeto a ser excluído está fora do escopo do registro atual.</span><span class="sxs-lookup"><span data-stu-id="8054b-324">The URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-325"><strong>3747</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-325"><strong>3747</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-326"><strong>adErrCatalogNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-326"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-327">A operação requer um <strong>ParentCatalog</strong> válido.</span><span class="sxs-lookup"><span data-stu-id="8054b-327">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-328"><strong>3748</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-328"><strong>3748</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-329"><strong>adErrCantChangeConnection</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-329"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p138">A conexão foi negada. A nova conexão que você solicitou possui características diferentes daquela que já está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="8054b-p138">Connection was denied. The new connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-332"><strong>3749</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-332"><strong>3749</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-333"><strong>adErrFieldsUpdateFailed</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-333"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-334">Falha na atualização de campos.</span><span class="sxs-lookup"><span data-stu-id="8054b-334">Fields update failed.</span></span> <span data-ttu-id="8054b-335">Para obter mais informações, examine a propriedade <strong>Status</strong> de objetos field individual.</span><span class="sxs-lookup"><span data-stu-id="8054b-335">For further information, examine the <strong>Status</strong> property of individual field objects.</span></span> <span data-ttu-id="8054b-336">Esse erro pode ocorrer em duas situações: quando alterando o valor de um objeto <strong>Field</strong> no processo de alterar ou adicionar um registro no banco de dados; e, ao alterar as propriedades do objeto <strong>Field</strong> em si.</span><span class="sxs-lookup"><span data-stu-id="8054b-336">This error can occur in two situations: when changing a <strong>Field</strong> object's value in the process of changing or adding a record to the database; and when changing the properties of the <strong>Field</strong> object itself.</span></span> <span data-ttu-id="8054b-337">A atualização de <strong>registro</strong> ou <strong>Recordset</strong> falhou devido a um problema com um dos campos no registro atual.</span><span class="sxs-lookup"><span data-stu-id="8054b-337">The <strong>Record</strong> or <strong>Recordset</strong> update failed due to a problem with one of the fields in the current record.</span></span> <span data-ttu-id="8054b-338">Enumere a coleção de <strong>campos</strong> e verifique se a propriedade <strong>Status</strong> de cada campo para determinar a causa do problema.</span><span class="sxs-lookup"><span data-stu-id="8054b-338">Enumerate the <strong>Fields</strong> collection and check the <strong>Status</strong> property of each field to determine the cause of the problem.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8054b-339"><strong>3750</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-339"><strong>3750</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-340"><strong>adErrDenyNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-340"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p140">O provedor não oferece suporte para restrições de compartilhamento. Foi feita uma tentativa de restringir o compartilhamento de arquivos e o seu provedor não oferece suporte para o conceito.</span><span class="sxs-lookup"><span data-stu-id="8054b-p140">Provider does not support sharing restrictions. An attempt was made to restrict file sharing and your provider does not support the concept.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8054b-343"><strong>3751</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-343"><strong>3751</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-344"><strong>adErrDenyTypeNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="8054b-344"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="8054b-p141">O provedor não oferece suporte para o tipo de restrição de compartilhamento solicitado. Foi feita uma tentativa de estabelecer um determinado tipo de restrição de compartilhamento de arquivos que não tem o suporte do provedor. Consulte a documentação do provedor para determinar quais são as restrições de compartilhamento de arquivos para as quais há suporte.</span><span class="sxs-lookup"><span data-stu-id="8054b-p141">Provider does not support the requested kind of sharing restriction. An attempt was made to establish a particular type of file-sharing restriction that is not supported by your provider. See the provider's documentation to determine what file-sharing restrictions are supported.</span></span></p></td>
</tr>
</tbody>
</table>

