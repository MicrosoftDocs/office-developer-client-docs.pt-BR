---
title: Método DeleteRecord (ADO)
TOCTitle: DeleteRecord method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d6ecd408bc2141ef9ff4bec8f6469a70e09bbe1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293991"
---
# <a name="deleterecord-method-ado"></a>Método DeleteRecord (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Exclui a entidade representada por um [Record](record-object-ado.md).

## <a name="syntax"></a>Sintaxe

*Record*. **DeleteRecord * * * Source*, *Async*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Source* |Opcional. Um valor **String** que contém uma URL que identifica a entidade (por exemplo, o arquivo ou diretório) a ser excluída. Se *Source* for omitido ou especificar uma sequência vazia, a entidade representada pelo [Record](record-object-ado.md) atual será excluída. Se o Record for um registro de coleção ([RecordType](recordtype-property-ado.md) de **adCollectionRecord**, tal como um diretório) todos os filhos (por exemplo, subdiretórios) também serão excluídos.|
|*Async* |Opcional. Um valor **Boolean** que, quando é **True**, especifica que a operação de exclusão é assíncrona.|

## <a name="remarks"></a>Comentários

As operações no objeto representado por esse **Record** podem falhar após a conclusão desse método. Depois de chamar **DeleteRecord**, o **Record** deve ser fechado porque o comportamento do **Record** pode ficar imprevisível dependendo de quando o provedor atualiza o **Record** com a fonte de dados.

Se esse **Record** foi obtido de um [Recordset](recordset-object-ado.md), os resultados dessa operação não serão refletidos imediatamente no **Recordset**. Atualize o **Recordset** fechando e reabrindo-o ou executando o **Recordset** [](requery-method-ado.md)Requery ou os métodos [Update](update-method-ado.md) e resync. [](resync-method-ado.md)

> [!NOTE]
> [!OBSERVAçãO] URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).


