---
title: Método CopyRecord (ADO)
TOCTitle: CopyRecord Method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5a54cf5f4d14b3e623a576dee99e1fabeb070e25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463714"
---
# <a name="copyrecord-method-ado"></a>Método CopyRecord (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Copia uma entidade representada por um **Record** para outro local.

## <a name="syntax"></a>Sintaxe

*Registro*. CopyRecord (*origem*, *destino*, *nome de usuário*, *senha*, *Opções*, *assíncrono*)

## <a name="parameters"></a>Parâmetros

  - *Source*

  - Opcional. Um valor **String** que contém uma URL que especifica a entidade a ser copiada (por exemplo, um arquivo ou diretório). Se a *fonte* for omitido ou especifica uma sequência vazia, o arquivo ou diretório representado pelo [registro](record-object-ado.md) atual será copiado.

  - *Destination*

  - Opcional. Um valor **String** que contém uma URL, especificando o local onde *fonte* serão copiados.

  - *UserName*

  - Opcional. Um valor **String** que contém o ID de usuário que, se necessário, autoriza acesso ao *Destination*.

  - *Password*

  - Opcional. Um valor **String** que contém a senha que, se necessária, verifica *UserName*.

  - *Options*

  - Opcional. Um valor [CopyRecordOptionsEnum](copyrecordoptionsenum.md) que tem o valor padrão **adCopyUnspecified**. Especifica o comportamento deste método.

  - *Async*

  - Opcional. Um valor **Boolean** que, quando é **True**, especifica que esta operação deve ser assíncrona.

## <a name="return-value"></a>Valor de Retorno

Um valor **String** que normalmente retorna o valor de *Destination*. No entanto, o valor exato retornado depende do provedor.

## <a name="remarks"></a>Comentários

Os valores de *origem* e de *destino* não devem ser idênticos; Caso contrário, ocorrerá um erro de tempo de execução. Pelo menos um dos nomes de servidor, caminho ou recurso deve ser diferente.

Todos os filhos (por exemplo, subdiretórios) de *Source* são copiados recursivamente, a menos que **adCopyNonRecursive** seja especificado. Em uma operação recursiva, *Destination* não deve ser um subdiretório de *Source*; caso contrário, a operação não será concluída.

Este método falha se *Destination* identificar uma entidade existente (por exemplo, um arquivo ou diretório), a menos que **adCopyOverWrite** seja especificado.


> [!IMPORTANT]
> <P>[!IMPORTANTE] Utilize a opção <STRONG>adCopyOverWrite</STRONG> criteriosamente. Por exemplo, se você especificar essa opção ao copiar um arquivo em um diretório irá <EM>Excluir</EM> o diretório e substituí-lo com o arquivo.</P>




> [!NOTE]
> <P>[!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obter mais informações, consulte <A href="absolute-and-relative-urls.md">URLs Absolutas e Relativas</A>.</P>

