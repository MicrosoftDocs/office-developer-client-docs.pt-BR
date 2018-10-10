---
title: Método AppendChunk (ADO)
TOCTitle: AppendChunk Method (ADO)
ms:assetid: 3fa931a3-2cd7-a3b0-a750-40e18bc9937e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249179(v=office.15)
ms:contentKeyID: 48544405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5a565430cf81eed5cbc1ebfe135ce80ee6f0177e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464859"
---
# <a name="appendchunk-method-ado"></a>Método AppendChunk (ADO)


**Aplica-se a**: Access 2013 | Office 2013


Acrescenta dados a um objeto [Field](field-object-ado.md) ou [Parameter](parameter-object-ado.md) de dados binários ou de texto longos.

## <a name="syntax"></a>Sintaxe

*objeto.* AppendChunk *dados*

## <a name="parameters"></a>Parâmetros

  - *object*

  - Um objeto **Field** ou **Parameter**.

  - *Data*

  - Um **Variant** que contém os dados a serem acrescentados ao objeto.

## <a name="remarks"></a>Comentários

Use o método **AppendChunk** em um objeto **Field** ou **Parameter** preenchê-lo com dados binários longos ou caracteres. Em situações em que a memória do sistema é limitada, você pode usar o método **AppendChunk** para manipular valores longos em partes, e não em sua totalidade.

**Objeto Field**

Se o bit **adFldLong** na propriedade [Attributes](attributes-property-ado.md) de um objeto **Field** for definido como true, você poderá usar o método **AppendChunk** para esse campo.

A primeira chamada de **AppendChunk** em um objeto **Field** grava dados no campo, substituindo os dados existentes. As chamadas subsequentes de **AppendChunk** são adicionadas aos dados existentes. Se você estiver acrescentando dados a um campo e, em seguida, definir ou ler o valor de outro campo no registro atual, o ADO assumirá que você concluiu o acréscimo de dados ao primeiro campo. Se você chamar o método **AppendChunk** novamente no primeiro campo, o ADO interpretará a chamada como uma nova operação **AppendChunk** e substituirá os dados existentes. O acesso a campos em outros objetos [Recordset](recordset-object-ado.md) que não sejam clones do primeiro objeto **Recordset** não interromperá as operações de **AppendChunk**.

Um erro ocorrerá se não houver registro atual quando você chamar **AppendChunk** em um objeto **Field**.


> [!NOTE]
> <P>[!OBSERVAçãO] O método <STRONG>AppendChunk</STRONG> não é operado nos objeto <STRONG>Field</STRONG> de um objeto <A href="record-object-ado.md">Record</A>. Ele não executa nenhuma operação e produzirá um erro em tempo de execução.</P>



**Objeto Parameter**

Se o bit **adParamLong** na propriedade **Attributes** de um objeto **Parameter** for definido como true, você poderá usar o método **AppendChunk** para esse parâmetro.

A primeira chamada de **AppendChunk** em um objeto **Parameter** grava dados no parâmetro, substituindo os dados existentes. As chamadas subsequentes de **AppendChunk** em um objeto **Parameter** são adicionadas aos dados de parâmetro existentes. A chamada de **AppendChunk** que passar um valor nulo descartará todos os dados de parâmetro.

