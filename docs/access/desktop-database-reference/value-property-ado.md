---
title: Propriedade Value (ADO)
TOCTitle: Value property (ADO)
ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15)
ms:contentKeyID: 48548958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 856f145c195c189775355fef662ea082ec629fd0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883936"
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
> <P>[!OBSERVAçãO] Para os objetos <STRONG>Parameter</STRONG>, o ADO lê a propriedade <STRONG>Value</STRONG> somente uma vez a partir do provedor. Se um comando contiver um <STRONG>Parameter</STRONG> cuja propriedade <STRONG>Value</STRONG> esteja vazia e você criar um <A href="recordset-object-ado.md">Recordset</A> a partir do comando, certifique-se de fechar o <STRONG>Recordset</STRONG> antes de recuperar a propriedade <STRONG>Value</STRONG>. Caso contrário, para alguns provedores, a propriedade <STRONG>Value</STRONG> poderá ficar vazia e não conterá o valor correto.</P>



Para novos objetos **Field** que foram acrescentados à coleção [Fields](fields-collection-ado.md) de um objeto [Record](record-object-ado.md), a propriedade **Value** deverá ser definida antes que qualquer outra propriedade **Field** seja especificada. Primeiro, um valor específico para a propriedade **Value** deve ser atribuído e o método [Update](update-method-ado.md) deve ser chamado na coleção **Fields**. Assim, outras propriedades, como [Type](type-property-ado.md) ou [Attributes](attributes-property-ado.md), poderão ser acessadas.

