---
title: Método CopyTo (ADO)
TOCTitle: CopyTo method (ADO)
ms:assetid: 1c1ab950-51f7-7ecc-ccd8-e689db02f06a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248958(v=office.15)
ms:contentKeyID: 48543558
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a17e74e1e3483b7ad2a70c5444503234cff5be12
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920246"
---
# <a name="copyto-method-ado"></a>Método CopyTo (ADO)


**Aplica-se a**: Access 2013, o Office 2013


Copia o número especificado de caracteres ou bytes (dependendo de [Type](type-property-ado-stream.md)) no [Stream](stream-object-ado.md) para outro objeto **Stream**.

## <a name="syntax"></a>Sintaxe

*Stream*. CopyTo *DestStream*, *NumChars*

## <a name="parameters"></a>Parâmetros

  - *DestStream*

  - Um valor de variável de objeto que contém uma referência para um objeto **Stream** aberto. O **Stream** atual é copiado para o **Stream** de destino especificado por *DestStream*. O **Stream** de destino já deve estar aberto. Se não estiver, ocorrerá um erro em tempo de execução.

   

    > [!NOTE]
    > O parâmetro *DestStream* não pode ser um proxy do objeto **Stream** porque isso requer acesso a uma interface particular no objeto **Stream** que não pode ser remota ao cliente.

  - *NumChars*

  - Opcional. Um valor **Integer** que especifica o número de bytes ou caracteres a serem copiados da posição atual no **Stream** de origem para o **Stream** de destino. O valor padrão é -1, que especifica que todos os caracteres ou bytes são copiados na posição atual para [EOS](eos-property-ado.md).

## <a name="remarks"></a>Comentários

Este método copia o número especificado de caracteres ou bytes, iniciando na posição atual especificada pela propriedade [Position](position-property-ado.md). Se o número especificado for maior que o número de bytes disponíveis até o **EOS**, apenas os caracteres ou bytes a partir da posição atual até o **EOS** serão copiados. Se o valor da *NumChars* é – 1 ou omitido, todos os caracteres ou bytes começando a partir da posição atual são copiados.

Se houver caracteres ou bytes existentes no fluxo de destino, todo o conteúdo além do ponto em que a cópia termina permanecerá e não será truncado. **Position** se torna o byte que segue imediatamente o último byte copiado. Se você deseja truncar esses bytes, chame [SetEOS](seteos-method-ado.md).

**CopyTo** deve ser utilizado para copiar dados para um **Stream** de destino do mesmo tipo que o **Stream** de origem (as definições de sua propriedade **Type** são ambas **adTypeText** ou ambas **adTypeBinary**). Para objetos **Stream** de texto, é possível alterar a definição da propriedade [Charset](charset-property-ado.md) do **Stream** de destino para converter de um conjunto de caracteres para outro. Além disso, objetos **Stream** de texto podem ser copiados com êxito para objetos **Stream** binários, mas objetos **Stream** binários não podem ser copiados para objetos **Stream** de texto.

