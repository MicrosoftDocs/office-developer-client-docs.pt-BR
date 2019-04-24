---
title: Método CopyRecord (ADO)
TOCTitle: CopyRecord method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5aac745bacf0662f6cd389bfefde7182a9676d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295524"
---
# <a name="copyrecord-method-ado"></a>Método CopyRecord (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Copia uma entidade representada por um **Record** para outro local.

## <a name="syntax"></a>Sintaxe

*Record*. CopyRecord (*origem*, *destino*, *nome de usuário*, *senha*, *Opções*, *assíncrono*)

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Source* |Opcional. Um valor **String** que contém uma URL que especifica a entidade a ser copiada (por exemplo, um arquivo ou diretório). Se *Source* for omitido ou especificar uma sequência vazia, o arquivo ou diretório representado pelo [Record](record-object-ado.md) atual será copiado.|
|*Destination* |Opcional. Um valor **String** que contém uma URL que especifica o local em que *Source* será copiado.|
|*UserName* |Opcional. Um valor **String** que contém o ID de usuário que, se necessário, autoriza acesso ao *Destination*.|
|*Password* |Opcional. Um valor **String** que contém a senha que, se necessária, verifica *UserName*.|
|*Options* |Opcional. Um valor [CopyRecordOptionsEnum](copyrecordoptionsenum.md) que tem o valor padrão **adCopyUnspecified**. Especifica o comportamento deste método.|
|*Async* |Opcional. Um valor **Boolean** que, quando é **True**, especifica que esta operação deve ser assíncrona.|

## <a name="return-value"></a>Valor de retorno

Um valor **String** que normalmente retorna o valor de *Destination*. No entanto, o valor exato retornado depende do provedor.

## <a name="remarks"></a>Comentários

Os valores de *Source* e *Destination* não devem ser idênticos; caso contrário, ocorrerá um erro em tempo de execução. Pelo menos um dos nomes de servidor, caminho ou recurso deve ser diferente.

Todos os filhos (por exemplo, subdiretórios) de *Source* são copiados recursivamente, a menos que **adCopyNonRecursive** seja especificado. Em uma operação recursiva, *Destination* não deve ser um subdiretório de *Source*; caso contrário, a operação não será concluída.

Este método falha se *Destination* identificar uma entidade existente (por exemplo, um arquivo ou diretório), a menos que **adCopyOverWrite** seja especificado.

> [!IMPORTANT]
> Utilize a opção **adCopyOverWrite** criteriosamente. Por exemplo, especificar essa opção ao copiar um arquivo para um diretório irá *excluir* o diretório e substituí-lo pelo arquivo.


> [!NOTE]
> [!OBSERVAçãO] URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).


