---
title: Método SetEOS (ADO)
TOCTitle: SetEOS method (ADO)
ms:assetid: d438eecf-7ab3-a07d-b6d5-8816db4aae7c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250063(v=office.15)
ms:contentKeyID: 48547933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b45e716844b3e616dfe5b8f94d69f29d6b0f1042
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997508"
---
# <a name="seteos-method-ado"></a>Método SetEOS (ADO)

**Aplica-se a**: Access 2013, o Office 2013

Define a posição que é o final do fluxo.

## <a name="syntax"></a>Sintaxe

*Stream*. SetEOS

## <a name="remarks"></a>Comentários

**SetEOS** atualiza o valor da propriedade [EOS](eos-property-ado.md), tornando a [Posição](position-property-ado.md) atual o final do fluxo. Quaisquer bytes ou caracteres após a posição atual serão truncados.

Como [Write](write-method-ado.md), [WriteText](writetext-method-ado.md) e [CopyTo](copyto-method-ado.md) não truncam nenhum valor extra nos objetos **Stream** existentes, você pode truncar esses bytes ou caracteres definindo a nova posição de final de fluxo com **SetEOS**.

> [!WARNING]
> Se você definir **EOS** para uma posição antes do final real do fluxo, perderá todos os dados após a nova posição de **EOS**.