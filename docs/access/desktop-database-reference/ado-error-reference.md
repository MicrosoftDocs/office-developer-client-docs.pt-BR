---
title: Referência de erros do ADO
TOCTitle: ADO error reference
ms:assetid: 21cec161-664a-4c18-4458-8117f4f63845
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248997(v=office.15)
ms:contentKeyID: 48543690
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a7f756af1422588d99fcffe1ae1413422131b70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283391"
---
# <a name="ado-error-reference"></a>Referência de erros do ADO

**Aplica-se ao:** Access 2013, Office 2013

A constante **ErrorValueEnum** descreve os valores de erro do ADO. Para obter uma listagem completa dessas constantes enumeradas, incluindo os valores, consulte [Apêndice B: erros do ADO](appendix-b-ado-errors.md). Esta seção examinará alguns dos erros mais interessantes e explicará algumas situações específicas que podem provocá-los, ou então as soluções para corrigir o problema. São listados a constante **ErrorValueEnum** e o número decimal positivo curto.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Número</p></th>
<th><p>Constante ErrorValueEnum</p></th>
<th><p>Descrição/causas possíveis</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>3000</strong></p></td>
<td><p><strong>adErrProviderFailed</strong></p></td>
<td><p>O provedor não pôde executar a operação solicitada.</p></td>
</tr>
<tr class="even">
<td><p><strong>3001</strong></p></td>
<td><p><strong>adErrInvalidArgument</strong></p></td>
<td><p>Os argumentos são do tipo incorreto, estão fora do intervalo aceitável ou há conflito entre eles. Este erro frequentemente é causado por um erro ortográfico em uma instrução SELECT do SQL. Por exemplo, um nome de campo ou de tabela incorreto. Este erro também pode ocorrer quando um campo ou uma tabela nomeada em uma instrução SELECT não existe no repositório de dados.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3002</strong></p></td>
<td><p><strong>adErrOpeningFile</strong></p></td>
<td><p>Não foi possível abrir o arquivo. Foi especificado um nome de arquivo incorreto, ou um arquivo foi movido, renomeado ou excluído. Em uma rede, a unidade pode estar temporariamente indisponível ou o tráfego da rede pode estar impedindo uma conexão.</p></td>
</tr>
<tr class="even">
<td><p><strong>3003</strong></p></td>
<td><p><strong>adErrReadFile</strong></p></td>
<td><p>Não foi possível ler o arquivo. O nome do arquivo está especificado incorretamente, o arquivo pode ter sido movido ou excluído, ou o arquivo pode ter sido corrompido.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3004</strong></p></td>
<td><p><strong>adErrWriteFile</strong></p></td>
<td><p>Falha ao gravar no arquivo. Talvez você tenha fechado um arquivo e, em seguida, tentado gravar nele, ou o arquivo pode estar corrompido. Se o arquivo estiver localizado em uma unidade de rede, as condições transitórias da rede podem impedir a gravação em uma unidade de rede.</p></td>
</tr>
<tr class="even">
<td><p><strong>3021</strong></p></td>
<td><p><strong>adErrNoCurrentRecord</strong></p></td>
<td><p><strong>BOF</strong> ou <strong>EOF</strong> é True ou o registro atual foi excluído. A operação solicitada requer um registro atual. Foi feita uma tentativa de atualizar os registros usando <strong>Find</strong> ou <strong>Seek</strong> para mover o ponteiro do registro para o registro desejado. Se o registro não for encontrado, <strong>EOF</strong> será True. Este erro também pode ocorrer após uma falha de <strong>AddNew</strong> ou <strong>Delete</strong> porque não existe nenhum registro atual quando esses métodos falham.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3219</strong></p></td>
<td><p><strong>adErrIllegalOperation</strong></p></td>
<td><p>A operação não é permitida neste contexto.</p></td>
</tr>
<tr class="even">
<td><p><strong>3220</strong></p></td>
<td><p><strong>adErrCantChangeProvider</strong></p></td>
<td><p>O provedor fornecido é diferente daquele que já está sendo usado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3246</strong></p></td>
<td><p><strong>adErrInTransaction</strong></p></td>
<td><p>O objeto <strong>Connection</strong> não pode ser fechado explicitamente durante uma transação. Um objeto <strong>Recordset</strong> ou <strong>Connection</strong> que está participando de uma transação no momento não pode ser fechado. Chame <strong>RollbackTrans</strong> ou <strong>CommitTrans</strong> antes de fechar o objeto.</p></td>
</tr>
<tr class="even">
<td><p><strong>3251</strong></p></td>
<td><p><strong>adErrFeatureNotAvailable</strong></p></td>
<td><p>O objeto ou provedor não consegue executar a operação solicitada. Algumas operações dependem de uma determinada versão do provedor.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3265</strong></p></td>
<td><p><strong>adErrItemNotFound</strong></p></td>
<td><p>O item não foi encontrado na coleção correspondente ao nome ou ordinal solicitado. Foi especificado um nome de campo ou de tabela incorreto.</p></td>
</tr>
<tr class="even">
<td><p><strong>3367</strong></p></td>
<td><p><strong>adErrObjectInCollection</strong></p></td>
<td><p>O objeto já está na coleção e não pode ser anexado. Não é possível adicionar um objeto à mesma coleção duas vezes.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3420</strong></p></td>
<td><p><strong>adErrObjectNotSet</strong></p></td>
<td><p>O objeto não é mais válido.</p></td>
</tr>
<tr class="even">
<td><p><strong>3421</strong></p></td>
<td><p><strong>adErrDataConversion</strong></p></td>
<td><p>O aplicativo usa um valor do tipo incorreto para a operação atual. Talvez você tenha fornecido uma sequência de caracteres para uma operação que espera um fluxo, por exemplo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3704</strong></p></td>
<td><p><strong>adErrObjectClosed</strong></p></td>
<td><p>A operação não é permitida quando o objeto está fechado. O objeto <strong>Connection</strong> ou <strong>Recordset</strong> foi fechado. Por exemplo, alguma outra rotina pode ter fechado um objeto global. Este erro pode ser evitado com a verificação da propriedade <strong>State</strong> antes de tentar uma operação.</p></td>
</tr>
<tr class="even">
<td><p><strong>3705</strong></p></td>
<td><p><strong>adErrObjectOpen</strong></p></td>
<td><p>A operação não é permitida quando o objeto está aberto. Um objeto aberto não pode estar aberto. Os campos não podem ser anexados a um <strong>Recordset</strong> aberto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3706</strong></p></td>
<td><p><strong>adErrProviderNotFound</strong></p></td>
<td><p>O provedor não pode ser localizado. Talvez ele não esteja instalado corretamente. O nome do provedor pode estar especificado incorretamente, o provedor especificado talvez não esteja instalado no computador em que o código está sendo executado, ou a instalação pode ter sido corrompida.</p></td>
</tr>
<tr class="even">
<td><p><strong>3707</strong></p></td>
<td><p><strong>adErrBoundToCommand</strong></p></td>
<td><p>A propriedade <strong>ActiveConnection</strong> de um objeto <strong>Recordset</strong>, que tem um objeto <strong>Command</strong> como fonte, não pode ser alterada. O aplicativo tentou atribuir um novo objeto <strong>Connection</strong> a um <strong>Recordset</strong> cuja fonte é um objeto <strong>Command</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3708</strong></p></td>
<td><p><strong>adErrInvalidParamInfo</strong></p></td>
<td><p>O objeto <strong>Parameter</strong> é definido de forma incorreta. Foram fornecidas informações inconsistentes ou incompletas.</p></td>
</tr>
<tr class="even">
<td><p><strong>3709</strong></p></td>
<td><p><strong>adErrInvalidConnection</strong></p></td>
<td><p>A conexão não pode ser usada para executar essa operação. Ela está fechada ou é inválida nesse contexto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3710</strong></p></td>
<td><p><strong>adErrNotReentrant</strong></p></td>
<td><p>A operação não pode ser executada durante o processamento do evento. Uma operação não pode ser executada em um manipulador de eventos que faz com que o evento seja acionado novamente. Por exemplo, os métodos de navegação não devem ser chamados a partir de um manipulador de eventos <strong>WillMove</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>3711</strong></p></td>
<td><p><strong>adErrStillExecuting</strong></p></td>
<td><p>A operação não pode ser executada durante a execução assíncrona.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3712</strong></p></td>
<td><p><strong>adErrOperationCancelled</strong></p></td>
<td><p>A operação foi cancelada pelo usuário. O aplicativo chamou o método <strong>CancelUpdate</strong> ou <strong>CancelBatch</strong> e a operação atual foi cancelada.</p></td>
</tr>
<tr class="even">
<td><p><strong>3713</strong></p></td>
<td><p><strong>adErrStillConnecting</strong></p></td>
<td><p>A operação não pode ser executada durante a conexão assíncrona.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3714</strong></p></td>
<td><p><strong>adErrInvalidTransaction</strong></p></td>
<td><p>A coordenação da transação é inválida ou não foi iniciada.</p></td>
</tr>
<tr class="even">
<td><p><strong>3715</strong></p></td>
<td><p><strong>adErrNotExecuting</strong></p></td>
<td><p>A operação não pode ser realizada enquanto não estiver sendo executada.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3716</strong></p></td>
<td><p><strong>adErrUnsafeOperation</strong></p></td>
<td><p>As configurações de segurança deste computador não permitem o acesso à fonte de dados em outro domínio.</p></td>
</tr>
<tr class="even">
<td><p><strong>3717</strong></p></td>
<td><p><strong>adWrnSecurityDialog</strong></p></td>
<td><p>Para uso interno apenas. Não use. (Entrada incluída para fins de complementação. Este erro não deve aparecer no seu código.)</p></td>
</tr>
<tr class="odd">
<td><p><strong>3718</strong></p></td>
<td><p><strong>adWrnSecurityDialogHeader</strong></p></td>
<td><p>Para uso interno apenas. Não use. (Entrada incluída para fins de complementação. Este erro não deve aparecer no seu código.)</p></td>
</tr>
<tr class="even">
<td><p><strong>3719</strong></p></td>
<td><p><strong>adErrIntegrityViolation</strong></p></td>
<td><p>Conflito entre valores de dados e as restrições de integridade do campo. Um novo valor para um <strong>Campo</strong> causaria uma chave duplicada. Um valor que forma um lado de uma relação entre dois registros pode não ser atualizável.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3720</strong></p></td>
<td><p><strong>adErrPermissionDenied</strong></p></td>
<td><p>A permissão insuficiente impede a gravação no campo. O usuário nomeado na sequência de conexão não tem as permissões adequadas para gravar em um <strong>Campo</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>3721</strong></p></td>
<td><p><strong>adErrDataOverflow</strong></p></td>
<td><p>O valor dos dados é muito grande para ser representado pelo tipo de dados do campo. Foi atribuído um valor numérico muito grande para o campo a que se destina. Por exemplo, um valor inteiro longo foi atribuído a um campo de inteiro curto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3722</strong></p></td>
<td><p><strong>adErrSchemaViolation</strong></p></td>
<td><p>Conflito entre valores de dados e o tipo de dados ou as restrições do campo. O repositório de dados possui restrições de validação diferentes do valor do <strong>Campo</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>3723</strong></p></td>
<td><p><strong>adErrSignMismatch</strong></p></td>
<td><p>A conversão falhou porque o valor dos dados era assinado e o tipo de dados do campo usado pelo provedor era não assinado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3724</strong></p></td>
<td><p><strong>adErrCantConvertvalue</strong></p></td>
<td><p>O valor dos dados não pode ser convertido por razões diferentes de incompatibilidade assinada ou estouro de dados. Por exemplo, a conversão teria truncado os dados.</p></td>
</tr>
<tr class="even">
<td><p><strong>3725</strong></p></td>
<td><p><strong>adErrCantCreate</strong></p></td>
<td><p>O valor dos dados não pode ser definido ou recuperado porque o tipo de dados do campo era desconhecido, ou os recursos do provedor eram insuficientes para executar a operação.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3726</strong></p></td>
<td><p><strong>adErrColumnNotOnThisRow</strong></p></td>
<td><p>O registro não contém esse campo. Foi especificado um nome de campo incorreto ou um campo que não está na coleção <strong>Fields</strong> do registro atual foi referenciado.</p></td>
</tr>
<tr class="even">
<td><p><strong>3727</strong></p></td>
<td><p><strong>adErrURLDoesNotExist</strong></p></td>
<td><p>A URL de origem ou o pai da URL de destino não existe. Há um erro ortográfico na URL de origem ou de destino. Você pode ter https://mysite/photo/myphoto.jpg quando deve realmente ter https://mysite/photos/myphoto.jpg em vez disso. O erro ortográfico na URL pai (neste caso, <em>photo</em> em vez de <em>photos</em>) causou o erro.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3728</strong></p></td>
<td><p><strong>adErrTreePermissionDenied</strong></p></td>
<td><p>As permissões são insuficientes para acessar a árvore ou subárvore. O usuário nomeado na sequência de conexão não tem as permissões adequadas.</p></td>
</tr>
<tr class="even">
<td><p><strong>3729</strong></p></td>
<td><p><strong>adErrInvalidURL</strong></p></td>
<td><p>A URL contém caracteres inválidos. Verifique se ela está digitada corretamente. A URL segue o esquema registrado para o provedor atual (por exemplo, Internet Publishing Provider está registrado para http).</p></td>
</tr>
<tr class="odd">
<td><p><strong>3730</strong></p></td>
<td><p><strong>adErrResourceLocked</strong></p></td>
<td><p>O objeto representado pela URL especificada está bloqueado por um ou mais processos. Aguarde a conclusão do processo e tente a operação novamente. O objeto que você está tentando acessar foi bloqueado por outro usuário ou por outro processo no seu aplicativo. É mais provável que isso aconteça em um ambiente multiusuário.</p></td>
</tr>
<tr class="even">
<td><p><strong>3731</strong></p></td>
<td><p><strong>adErrResourceExists</strong></p></td>
<td><p>A operação de cópia não pode ser executada. O objeto nomeado pela URL de destino já existe. Especifique <strong>adCopyOverwrite</strong> para substituí-lo. Se você não especificar <strong>adCopyOverwrite</strong> ao copiar os arquivos em um diretório, haverá falha quando você tentar copiar um item que já existe no local de destino.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3732</strong></p></td>
<td><p><strong>adErrCannotComplete</strong></p></td>
<td><p>O servidor não pode concluir a operação. Isso pode ocorrer porque o servidor está ocupado com outras operações ou porque os recursos do servidor são insuficientes.</p></td>
</tr>
<tr class="even">
<td><p><strong>3733</strong></p></td>
<td><p><strong>adErrVolumeNotFound</strong></p></td>
<td><p>O provedor não pode localizar o dispositivo de repositório indicado pela URL. Verifique se a URL está digitada corretamente. A URL do dispositivo de repositório pode estar incorreta, mas este erro pode ocorrer por outros motivos. É possível que o dispositivo esteja offline ou um grande volume de tráfego da rede pode impedir que a conexão seja estabelecida.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3734</strong></p></td>
<td><p><strong>adErrOutOfSpace</strong></p></td>
<td><p>A operação não pode ser executada. O provedor não pode obter espaço de repositório suficiente. Talvez não haja RAM ou espaço no disco rígido suficiente para os arquivos temporários no servidor.</p></td>
</tr>
<tr class="even">
<td><p><strong>3735</strong></p></td>
<td><p><strong>adErrResourceOutOfScope</strong></p></td>
<td><p>A URL de origem ou de destino está fora do escopo do registro atual.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3736</strong></p></td>
<td><p><strong>adErrUnavailable</strong></p></td>
<td><p>A operação não pôde ser concluída e o status não está disponível. O campo pode estar indisponível ou a operação não foi tentada. Outro usuário pode ter alterado ou excluído o campo que você está tentando acessar.</p></td>
</tr>
<tr class="even">
<td><p><strong>3737</strong></p></td>
<td><p><strong>adErrURLNamedRowDoesNotExist</strong></p></td>
<td><p>O registro nomeado por essa URL não existe. Durante a tentativa de abrir um arquivo usando um objeto <strong>Record</strong>, o nome do arquivo ou o caminho para o arquivo estava incorreto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3738</strong></p></td>
<td><p><strong>adErrDelResOutOfScope</strong></p></td>
<td><p>A URL do objeto a ser excluído está fora do escopo do registro atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>3747</strong></p></td>
<td><p><strong>adErrCatalogNotSet</strong></p></td>
<td><p>A operação requer um <strong>ParentCatalog</strong> válido.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3748</strong></p></td>
<td><p><strong>adErrCantChangeConnection</strong></p></td>
<td><p>A conexão foi negada. A nova conexão que você solicitou possui características diferentes daquela que já está sendo usada.</p></td>
</tr>
<tr class="even">
<td><p><strong>3749</strong></p></td>
<td><p><strong>adErrFieldsUpdateFailed</strong></p></td>
<td><p>A atualização dos campos falhou. Para obter mais informações, examine a propriedade <strong>Status</strong> de objetos de campo individuais. Este erro pode ocorrer em duas situações: ao alterar o valor de um objeto <strong>Field</strong> no processo de alteração ou inclusão de um registro no banco de dados; e ao alterar as propriedades do próprio campo <strong>Field</strong>. Falha na atualização de <strong>Record</strong> ou <strong>Recordset</strong> devido a um problema com um dos campos do registro atual. Enumere a coleção <strong>Fields</strong> e verifique a propriedade <strong>Status</strong> de cada campo para determinar a causa do problema.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3750</strong></p></td>
<td><p><strong>adErrDenyNotSupported</strong></p></td>
<td><p>O provedor não oferece suporte para restrições de compartilhamento. Foi feita uma tentativa de restringir o compartilhamento de arquivos e o seu provedor não oferece suporte para o conceito.</p></td>
</tr>
<tr class="even">
<td><p><strong>3751</strong></p></td>
<td><p><strong>adErrDenyTypeNotSupported</strong></p></td>
<td><p>O provedor não oferece suporte para o tipo de restrição de compartilhamento solicitado. Foi feita uma tentativa de estabelecer um determinado tipo de restrição de compartilhamento de arquivos que não tem o suporte do provedor. Consulte a documentação do provedor para determinar quais são as restrições de compartilhamento de arquivos para as quais há suporte.</p></td>
</tr>
</tbody>
</table>

