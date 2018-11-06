---
title: Método MoveRecord (ADO)
TOCTitle: MoveRecord method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 022db96a00253793505df6e89603070a6d429a8d
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998865"
---
# <a name="moverecord-method-ado"></a>Método MoveRecord (ADO)

**Aplica-se a**: Access 2013, o Office 2013
 
Move a entidade representada por um [Record](record-object-ado.md) para outro local.

## <a name="syntax"></a>Sintaxe

*Registro*. MoveRecord (*origem*, *destino*, *nome de usuário*, *senha*, *Opções*, *assíncrono*)

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Origem* |Opcional. Um valor **String** que contém uma URL que identifica o **Record** a ser movido. Se *Source* for omitido ou especificar uma sequência vazia, o objeto representado por este **Record** será movido. Por exemplo, se o **Record** representar um arquivo, o conteúdo do arquivo será movido para o local especificado por *Destination*.|
|*Destination* |Opcional. Um valor **String** que contém uma URL, especificando o local onde *fonte* será movido.|
|*UserName* |Opcional. Um valor **String** que contém o ID de usuário que, se necessário, autoriza acesso ao *Destination*.|
|*Password* |Opcional. Uma **String** que contém a senha que, se necessária, verifica *UserName*.|
|*Options* |Opcional. Um valor [MoveRecordOptionsEnum](moverecordoptionsenum.md) cujo valor padrão é **adMoveUnspecified**. Especifica o comportamento deste método.|
|*Async* |Opcional. **Boolean** valor que, quando especifica **True**, esta operação deve ser assíncrona.|

## <a name="return-value"></a>Valor de retorno

Um valor **String**. Geralmente, é retornado o valor de *destino* . No entanto, o valor exato retornado depende do provedor.

## <a name="remarks"></a>Comentários

Os valores de *origem* e de *destino* não devem ser idênticos; Caso contrário, ocorrerá um erro de tempo de execução. Pelo menos os nomes de servidor, caminho e recurso devem ser diferentes.

Para arquivos movidos utilizando-se o Internet Publishing Provider, este método atualiza todos os links de hipertexto nos arquivos que estão sendo movidos, a menos que especificado o contrário por *Options*. Este método falha se *Destination* identificar um objeto existente (por exemplo, um arquivo ou diretório), a menos que **adMoveOverWrite** seja especificado.

> [!NOTE]
> [!OBSERVAçãO] Utilize a opção **adMoveOverWrite** criteriosamente. Por exemplo, especificar essa opção ao mover um arquivo para um diretório irá excluir o diretório e substituí-lo pelo arquivo.

Alguns atributos do objeto **Record**, tal como a propriedade [ParentURL](parenturl-property-ado.md), não serão atualizados após a conclusão dessa operação. Atualize as propriedades do objeto **Record** fechando o **Record** e, em seguida, reabrindo-o com a URL do local em que o arquivo ou diretório foi movido.

Se esse **Record** foi obtido de um [Recordset](recordset-object-ado.md), o novo local do arquivo ou diretório movido não será refletido imediatamente no **Recordset**. Atualize o **Recordset** fechando e reabrindo o mesmo.

> [!NOTE]
> [!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).


