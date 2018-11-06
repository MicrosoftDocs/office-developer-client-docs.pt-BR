---
title: Propriedade Value (ADO)
TOCTitle: Value property (ADO)
ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15)
ms:contentKeyID: 48548958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a61803648a0efa5f226b222fb54ce96c8aadbfe
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999054"
---
# <a name="value-property-ado"></a>Propriedade Value (ADO)

**Aplica-se a**: Access 2013, o Office 2013

Indica o valor atribuído a um objeto [Field](field-object-ado.md), [Parameter](parameter-object-ado.md) ou [Property](property-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Variant** que indica o valor do objeto. O valor padrão depende da propriedade [Type](type-property-ado.md).

## <a name="remarks"></a>Comentários

Utilize a propriedade **Value** para definir ou retornar dados a partir dos objetos **Field**, para definir ou retornar valores de parâmetro com os objetos **Parameter**, ou para definir ou retornar definições de propriedade com os objetos **Property**. A definição da propriedade **Value** como leitura/gravação ou somente leitura depende de diversos fatores  consulte os tópicos do respectivo objeto para obter mais informações.

O ADO permite a definição e o retorno de dados binários longos com a propriedade **Value**.

> [!NOTE]
> [!OBSERVAçãO] Para os objetos **Parameter**, o ADO lê a propriedade **Value** somente uma vez a partir do provedor. Se um comando contiver um **Parameter** cuja propriedade **Value** esteja vazia e você criar um [Recordset](recordset-object-ado.md) a partir do comando, certifique-se de fechar o **Recordset** antes de recuperar a propriedade **Value**. Caso contrário, para alguns provedores, a propriedade **Value** poderá ficar vazia e não conterá o valor correto.

Para novos objetos **Field** que foram acrescentados à coleção [Fields](fields-collection-ado.md) de um objeto [Record](record-object-ado.md), a propriedade **Value** deverá ser definida antes que qualquer outra propriedade **Field** seja especificada. Primeiro, um valor específico para a propriedade **Value** deve ser atribuído e o método [Update](update-method-ado.md) deve ser chamado na coleção **Fields**. Assim, outras propriedades, como [Type](type-property-ado.md) ou [Attributes](attributes-property-ado.md), poderão ser acessadas.

