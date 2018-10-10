---
title: ErrorValueEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ErrorValueEnum
ms:assetid: 2af99f32-6004-1225-367c-45d693f447b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249058(v=office.15)
ms:contentKeyID: 48543921
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de7f19c119c3161ece57344b911fcca36a1a8a3d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463876"
---
# <a name="errorvalueenum"></a>ErrorValueEnum


**Aplica-se a**: Access 2013 | Office 2013

Especifica o tipo de erro de tempo de execução do ADO.

Três formatos de número de erro são listados:

  - Decimal positivo  os dois bytes baixos de um número completo em formato decimal. Esse número é exibido na caixa de diálogo de erros padrão do Visual Basic. Por exemplo, Erro de tempo de execução '3707'.

  - Decimal negativo  A conversão decimal de um número completo do erro.

  - Hexadecimal  — A representação hexadecimal do número completo do erro. O código de recurso do Windows está no quarto dígito. O código de recurso para números de erro do ADO é *A*. Por exemplo: 0x800***A***0E7B.


> [!NOTE]
> <P>Os erros do OLE DB podem ser transmitidos para seu aplicativo ADO. Em geral, eles podem ser identificados por um código de recursos do Windows de <EM>4</EM>. Por exemplo, 0x800<STRONG><EM>4</EM></STRONG>.... Para obter mais informações sobre esses números, consulte o Capítulo 16 do manual <EM>OLE DB Programmer's Reference (Referência para programadores do OLE DB)</EM>.</P>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adErrBoundToCommand</strong></p></td>
<td><p>3707<br />
-2146824581<br />
0x800A0E7B</p></td>
<td><p>Não pode alterar a propriedade <strong>ActiveConnection</strong> de um objeto <strong>Recordset</strong> que tem um objeto <strong>Command</strong> como sua fonte.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrCannotComplete</strong></p></td>
<td><p>3732<br />
-2146824556<br />
0x800A0E94</p></td>
<td><p>O servidor não pode concluir a operação.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrCantChangeConnection</strong></p></td>
<td><p>3748<br />
-2146824540<br />
0x800A0EA4</p></td>
<td><p>A conexão foi negada. A nova conexão solicitada tem diferentes recursos em relação àquela que está em uso.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrCantChangeProvider</strong></p></td>
<td><p>3220<br />
-2146825068<br />
0X800A0C94</p></td>
<td><p>O provedor designado é diferente daquele que está em uso.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrCantConvertvalue</strong></p></td>
<td><p>3724<br />
-2146824564<br />
0x800A0E8C</p></td>
<td><p>O valor dos dados não pode ser convertido por razões diferentes de incompatibilidade assinada ou estouro de dados. Por exemplo, a conversão truncaria os dados.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrCantCreate</strong></p></td>
<td><p>3725<br />
-2146824563<br />
0x800A0E8D</p></td>
<td><p>O valor dos dados não pode ser definido ou recuperado porque o tipo de dados do campo é desconhecido ou o provedor tem recursos insuficientes para executar a operação.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrCatalogNotSet</strong></p></td>
<td><p>3747<br />
-2146824541<br />
0x800A0EA3</p></td>
<td><p>A operação requer um <strong>ParentCatalog</strong> válido.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrColumnNotOnThisRow</strong></p></td>
<td><p>3726<br />
-2146824562<br />
0x800A0E8E</p></td>
<td><p>O registro não contém esse campo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrDataConversion</strong></p></td>
<td><p>3421<br />
-2146824867<br />
0x800A0D5D</p></td>
<td><p>O aplicativo usa um valor de tipo incorreto para a operação atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrDataOverflow</strong></p></td>
<td><p>3721<br />
-2146824567<br />
0x800A0E89</p></td>
<td><p>O valor dos dados é muito grande para ser representado pelo tipo de dados do campo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrDelResOutOfScope</strong></p></td>
<td><p>3738<br />
-2146824550<br />
0x800A0E9A</p></td>
<td><p>A URL do objeto a ser excluído está fora do escopo do registro atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrDenyNotSupported</strong></p></td>
<td><p>3750<br />
-2146824538<br />
0x800A0EA6</p></td>
<td><p>O provedor não oferece suporte a restrições de compartilhamento.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrDenyTypeNotSupported</strong></p></td>
<td><p>3751<br />
-2146824537<br />
0x800A0EA7</p></td>
<td><p>O provedor não oferece suporte ao tipo solicitado de restrição de compartilhamento.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrFeatureNotAvailable</strong></p></td>
<td><p>3251<br />
-2146825037<br />
0x800A0CB3</p></td>
<td><p>O objeto ou o provedor não pode executar a operação solicitada.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrFieldsUpdateFailed</strong></p></td>
<td><p>3749<br />
-2146824539<br />
0x800A0EA5</p></td>
<td><p>A atualização dos campos falhou. Para obter outras informações, analise a propriedade <strong>Status</strong> dos objetos de campo individuais.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrIllegalOperation</strong></p></td>
<td><p>3219<br />
-2146825069<br />
0x800A0C93</p></td>
<td><p>A operação não é permitida nesse contexto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrIntegrityViolation</strong></p></td>
<td><p>3719<br />
-2146824569<br />
0x800A0E87</p></td>
<td><p>O valor de dados está em conflito com as restrições de integridade do campo.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrInTransaction</strong></p></td>
<td><p>3246<br />
-2146825042<br />
0x800A0CAE</p></td>
<td><p>O objeto <strong>Connection</strong> não pode ser explicitamente fechado durante uma transação.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrInvalidArgument</strong></p></td>
<td><p>3001<br />
-2146825287<br />
0x800A0BB9</p></td>
<td><p>Os argumentos são do tipo incorreto, estão fora do intervalo aceitável ou estão em conflito uns com os outros.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrInvalidConnection</strong></p></td>
<td><p>3709<br />
-2146824579<br />
0x800A0E7D</p></td>
<td><p>A conexão não pode ser usada para executar essa operação. Ela está fechada ou é inválida nesse contexto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrInvalidParamInfo</strong></p></td>
<td><p>3708<br />
-2146824580<br />
0x800A0E7C</p></td>
<td><p>O objeto <strong>Parameter</strong> é definido de forma incorreta. Foram fornecidas informações inconsistentes ou incompletas.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrInvalidTransaction</strong></p></td>
<td><p>3714<br />
-2146824574<br />
0x800A0E82</p></td>
<td><p>A transação de coordenação é inválida ou não foi iniciada.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrInvalidURL</strong></p></td>
<td><p>3729<br />
-2146824559<br />
0x800A0E91</p></td>
<td><p>A URL contém caracteres inválidos. Certifique-se de que a URL esteja digitada corretamente.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrItemNotFound</strong></p></td>
<td><p>3265<br />
-2146825023<br />
0x800A0CC1</p></td>
<td><p>O item não pode ser localizado na coleção correspondente para o nome ou ordinal solicitado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrNoCurrentRecord</strong></p></td>
<td><p>3021<br />
-2146825267<br />
0x800A0BCD</p></td>
<td><p><strong>BOF</strong> ou <strong>EOF</strong> é True ou o registro atual foi excluído. A operação solicitada requer um registro atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrNotExecuting</strong></p></td>
<td><p>3715<br />
-2146824573<br />
0x800A0E83</p></td>
<td><p>A operação não pode ser executada sozinha.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrNotReentrant</strong></p></td>
<td><p>3710<br />
-2146824578<br />
0x800A0E7E</p></td>
<td><p>A operação não pode ser executada durante o processamento do evento.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrObjectClosed</strong></p></td>
<td><p>3704<br />
-2146824584<br />
0x800A0E78</p></td>
<td><p>A operação não é permitida quando o objeto está fechado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrObjectInCollection</strong></p></td>
<td><p>3367<br />
-2146824921<br />
0x800A0D27</p></td>
<td><p>O objeto já está na coleção. Não é possível anexá-lo.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrObjectNotSet</strong></p></td>
<td><p>3420<br />
-2146824868<br />
0x800A0D5C</p></td>
<td><p>O objeto não é mais válido.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrObjectOpen</strong></p></td>
<td><p>3705<br />
-2146824583<br />
0x800A0E79</p></td>
<td><p>A operação não é permitida quando o objeto está aberto.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrOpeningFile</strong></p></td>
<td><p>3002<br />
-2146825286<br />
0x800A0BBA</p></td>
<td><p>O arquivo não pôde ser aberto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrOperationCancelled</strong></p></td>
<td><p>3712<br />
-2146824576<br />
0x800A0E80</p></td>
<td><p>A operação foi cancelada pelo usuário.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrOutOfSpace</strong></p></td>
<td><p>3734<br />
-2146824554<br />
0x800A0E96</p></td>
<td><p>A operação não pode ser executada. O provedor não pode obter espaço de repositório suficiente.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrPermissionDenied</strong></p></td>
<td><p>3720<br />
-2146824568<br />
0x800A0E88</p></td>
<td><p>Permissão insuficiente impede escrever no campo.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrProviderFailed</strong></p></td>
<td><p>3000<br />
-2146825288<br />
0x800A0BB8</p></td>
<td><p>O provedor falhou em executar a operação solicitada.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrProviderNotFound</strong></p></td>
<td><p>3706<br />
-2146824582<br />
0x800A0E7A</p></td>
<td><p>O provedor não pode ser localizado. Ele não pode ser instalado corretamente.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrReadFile</strong></p></td>
<td><p>3003<br />
-2146825285<br />
0x800A0BBB</p></td>
<td><p>O arquivo não pôde ser lido.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrResourceExists</strong></p></td>
<td><p>3731<br />
-2146824557<br />
0x800A0E93</p></td>
<td><p>A operação Copy não pode ser executada. O objeto nomeado pela URL de destino já existe. Especifique <strong>adCopyOverwrite</strong> para substituir o objeto.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrResourceLocked</strong></p></td>
<td><p>3730<br />
-2146824558<br />
0x800A0E92</p></td>
<td><p>O objeto representado pela URL especificada está bloqueado por um ou mais processos diferentes. Aguarde até que o processo seja finalizado e tente executar a operação novamente.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrResourceOutOfScope</strong></p></td>
<td><p>3735<br />
-2146824553<br />
0x800A0E97</p></td>
<td><p>A URL de origem ou de destino está fora do escopo do registro atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrSchemaViolation</strong></p></td>
<td><p>3722<br />
-2146824566<br />
0x800A0E8A</p></td>
<td><p>O valor dos dados está em conflito com o tipo de dados ou com as restrições do campo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrSignMismatch</strong></p></td>
<td><p>3723<br />
-2146824565<br />
0x800A0E8B</p></td>
<td><p>A conversão falhou porque o valor dos dados era assinado e o tipo de dados do campo utilizado pelo provedor não era.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrStillConnecting</strong></p></td>
<td><p>3713<br />
-2146824575<br />
0x800A0E81</p></td>
<td><p>A operação não pode ser executado durante uma conexão assíncrona.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrStillExecuting</strong></p></td>
<td><p>3711<br />
-2146824577<br />
0x800A0E7F</p></td>
<td><p>A operação não pode ser executada durante uma execução assíncrona.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrTreePermissionDenied</strong></p></td>
<td><p>3728<br />
-2146824560<br />
0x800A0E90</p></td>
<td><p>As permissões são insuficientes para acessar a árvore ou a subárvore.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrUnavailable</strong></p></td>
<td><p>3736<br />
-2146824552<br />
0x800A0E98</p></td>
<td><p>Houve falha na conclusão da operação, e o status não está disponível. O campo pode estar indisponível ou a operação não foi repetida.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrUnsafeOperation</strong></p></td>
<td><p>3716<br />
-2146824572<br />
0x800A0E84</p></td>
<td><p>As configurações de segurança nesse computador proíbem o acesso à fonte de dados em outro domínio.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrURLDoesNotExist</strong></p></td>
<td><p>3727<br />
-2146824561<br />
0x800A0E8F</p></td>
<td><p>A URL de origem ou o pai da URL de destino não existe.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrURLNamedRowDoesNotExist</strong></p></td>
<td><p>3737<br />
-2146824551<br />
0x800A0E99</p></td>
<td><p>O registro chamado por essa URL não existe.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrVolumeNotFound</strong></p></td>
<td><p>3733<br />
-2146824555<br />
0x800A0E95</p></td>
<td><p>O provedor não pode localizar o dispositivo de repositório indicado pela URL. Certifique-se de que a URL esteja digitada corretamente.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrWriteFile</strong></p></td>
<td><p>3004<br />
-2146825284<br />
0x800A0BBC</p></td>
<td><p>Falha ao gravar no arquivo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adWrnSecurityDialog</strong></p></td>
<td><p>3717<br />
-2146824571<br />
0x800A0E85</p></td>
<td><p>Para uso interno apenas. Não use.</p></td>
</tr>
<tr class="even">
<td><p><strong>adWrnSecurityDialogHeader</strong></p></td>
<td><p>3718<br />
-2146824570<br />
0x800A0E86</p></td>
<td><p>Para uso interno apenas. Não use.</p></td>
</tr>
</tbody>
</table>


**ADO/WFC Equivalente**

Pacote: **com.ms.wfc.data**

Somente os seguintes subconjuntos de equivalentes do ADO/WFC estão definidos.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.BOUNDTOCOMMAND</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.DATACONVERSION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.FEATURENOTAVAILABLE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.ILLEGALOPERATION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.INTRANSACTION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.INVALIDARGUMENT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.INVALIDCONNECTION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.INVALIDPARAMINFO</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.ITEMNOTFOUND</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.NOCURRENTRECORD</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.NOTEXECUTING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.NOTREENTRANT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.OBJECTCLOSED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.OBJECTINCOLLECTION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.OBJECTNOTSET</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.OBJECTOPEN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.OPERATIONCANCELLED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.PROVIDERNOTFOUND</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.STILLCONNECTING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.STILLEXECUTING</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.UNSAFEOPERATION</p></td>
</tr>
</tbody>
</table>

