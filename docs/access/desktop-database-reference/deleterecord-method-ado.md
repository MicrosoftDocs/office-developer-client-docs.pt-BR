---
title: Método DeleteRecord (ADO)
TOCTitle: DeleteRecord Method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d850234faf18a2bd6f3278ee4feade3aa3bb561
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462148"
---
# <a name="deleterecord-method-ado"></a>Método DeleteRecord (ADO)


**Aplica-se a**: Access 2013 | Office 2013



Exclui a entidade representada por um [Record](record-object-ado.md).

## <a name="syntax"></a>Sintaxe

*Registro*. **ExcluirRegistro * * * fonte*, *assíncrono*

## <a name="parameters"></a>Parâmetros

  - *Source*

  - Opcional. Um valor **String** que contém uma URL que identifica a entidade (por exemplo, o arquivo ou diretório) a ser excluída. Se *Source* for omitido ou especificar uma sequência vazia, a entidade representada pelo [Record](record-object-ado.md) atual será excluída. Se o Record for um registro de coleção ([RecordType](recordtype-property-ado.md) de **adCollectionRecord**, tal como um diretório) todos os filhos (por exemplo, subdiretórios) também serão excluídos.

  - *Async*

  - Opcional. Um valor **Boolean** que, quando é **True**, especifica que a operação de exclusão é assíncrona.

## <a name="remarks"></a>Comentários

As operações no objeto representado por esse **Record** podem falhar após a conclusão desse método. Depois de chamar **DeleteRecord**, o **Record** deve ser fechado porque o comportamento do **Record** pode ficar imprevisível dependendo de quando o provedor atualiza o **Record** com a fonte de dados.

Se esse **Record** foi obtido de um [Recordset](recordset-object-ado.md), os resultados dessa operação não serão refletidos imediatamente no **Recordset**. Atualize o **Recordset** fechando e abrindo-o novamente, ou os métodos **Recordset** [Requery](requery-method-ado.md), ou [Update](update-method-ado.md) e [Resync](resync-method-ado.md) executá-lo.


> [!NOTE]
> <P>[!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obter mais informações, consulte <A href="absolute-and-relative-urls.md">URLs Absolutas e Relativas</A>.</P>

