---
title: Método MoveRecord (ADO)
TOCTitle: MoveRecord method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c9937f0ab32c5dba0e4435fdc0ba7e111f5651dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288676"
---
# <a name="moverecord-method-ado"></a>Método MoveRecord (ADO)

**Aplica-se ao:** Access 2013, Office 2013
 
Move a entidade representada por um [Record](record-object-ado.md) para outro local.

## <a name="syntax"></a>Sintaxe

*Registro*. MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Source* |Opcional. Um valor **String** que contém uma URL que identifica o **Record** a ser movido. Se *Source* for omitido ou especificar uma sequência vazia, o objeto representado por este **Record** será movido. Por exemplo, se o **Record** representar um arquivo, o conteúdo do arquivo será movido para o local especificado por *Destination*.|
|*Destination* |Opcional. Um valor **String** que contém uma URL que especifica o local em que *Source* será movido.|
|*UserName* |Opcional. Um valor **String** que contém o ID de usuário que, se necessário, autoriza acesso ao *Destination*.|
|*Password* |Opcional. Uma **String** que contém a senha que, se necessária, verifica *UserName*.|
|*Options* |Opcional. Um valor [MoveRecordOptionsEnum](moverecordoptionsenum.md) cujo valor padrão é **adMoveUnspecified**. Especifica o comportamento deste método.|
|*Async* |Opcional. Um **valor Boolean** que, **quando True**, especifica que esta operação deve ser assíncrona.|

## <a name="return-value"></a>Valor de retorno

Um valor **String**. Normalmente, o valor de *Destination* é retornado. No entanto, o valor exato retornado depende do provedor.

## <a name="remarks"></a>Comentários

Os valores de *Source* e *Destination* não devem ser idênticos; caso contrário, ocorrerá um erro em tempo de execução. Pelo menos os nomes de servidor, caminho e recurso devem ser diferentes.

Para arquivos movidos utilizando-se o Internet Publishing Provider, este método atualiza todos os links de hipertexto nos arquivos que estão sendo movidos, a menos que especificado o contrário por *Options*. Este método falha se *Destination* identificar um objeto existente (por exemplo, um arquivo ou diretório), a menos que **adMoveOverWrite** seja especificado.

> [!NOTE]
> [!OBSERVAçãO] Utilize a opção **adMoveOverWrite** criteriosamente. Por exemplo, especificar essa opção ao mover um arquivo para um diretório irá excluir o diretório e substituí-lo pelo arquivo.

Alguns atributos do objeto **Record**, tal como a propriedade [ParentURL](parenturl-property-ado.md), não serão atualizados após a conclusão dessa operação. Atualize as propriedades do objeto **Record** fechando o **Record** e, em seguida, reabrindo-o com a URL do local em que o arquivo ou diretório foi movido.

Se esse **Record** foi obtido de um [Recordset](recordset-object-ado.md), o novo local do arquivo ou diretório movido não será refletido imediatamente no **Recordset**. Atualize o **Recordset** fechando e reabrindo o mesmo.

> [!NOTE]
> [!OBSERVAçãO] URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obter mais informações, consulte [URLs absolutas e relativas.](absolute-and-relative-urls.md)


