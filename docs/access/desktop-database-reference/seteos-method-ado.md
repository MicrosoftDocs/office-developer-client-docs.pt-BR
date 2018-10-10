---
title: Método SetEOS (ADO)
TOCTitle: SetEOS Method (ADO)
ms:assetid: d438eecf-7ab3-a07d-b6d5-8816db4aae7c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250063(v=office.15)
ms:contentKeyID: 48547933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 456bbf7c7235d0db01b29372ee8f70c364263cb6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461952"
---
# <a name="seteos-method-ado"></a>Método SetEOS (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Define a posição que é o final do fluxo.

## <a name="syntax"></a>Sintaxe

*Stream*. SetEOS

## <a name="remarks"></a>Comentários

**SetEOS** atualiza o valor da propriedade [EOS](eos-property-ado.md), tornando a [Posição](position-property-ado.md) atual o final do fluxo. Quaisquer bytes ou caracteres após a posição atual serão truncados.

Como [Write](write-method-ado.md), [WriteText](writetext-method-ado.md) e [CopyTo](copyto-method-ado.md) não truncam nenhum valor extra nos objetos **Stream** existentes, você pode truncar esses bytes ou caracteres definindo a nova posição de final de fluxo com **SetEOS**.


> [!WARNING]
> <P>Se você definir <STRONG>EOS</STRONG> para uma posição antes do final real do fluxo, perderá todos os dados após a nova posição de <STRONG>EOS</STRONG>.</P>


