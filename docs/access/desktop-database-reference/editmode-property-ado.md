---
title: Propriedade EditMode (ADO)
TOCTitle: EditMode property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d7bba0af804df89bf4c8611e184928c9bf12d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293606"
---
# <a name="editmode-property-ado"></a>Propriedade EditMode (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica o status de edição do registro atual.

## <a name="return-value"></a>Valor de retorno

Retorna um valor [EditModeEnum](editmodeenum.md).

## <a name="remarks"></a>Comentários

O ADO mantém um buffer de edição associado ao registro atual. Essa propriedade indica se as alterações foram feitas nesse buffer ou se um novo registro foi criado. Use a propriedade **EditMode** para determinar o status de edição do registro atual. É possível procurar alterações pendentes se um processo de edição tiver sido interrompido e determinar se você precisa usar o método [Update](update-method-ado.md) ou [CancelUpdate](cancelupdate-method-ado.md).

Consulte o método [AddNew](addnew-method-ado.md) para obter uma descrição mais detalhada da propriedade **EditMode** em diferentes condições de edição.

Quando uma [](delete-method-ado-recordset.md) chamada para Excluir não exclui com êxito o registro ou registros na fonte de dados (devido a violações de integridade referencial, por exemplo), o [Recordset](recordset-object-ado.md) permanecerá no modo de edição (**EditMode**  =  **adEditInProgress**). Isso significa que **CancelUpdate** deve ser chamado antes de sair do registro atual (com [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) ou [Close](close-method-ado.md), por exemplo).


> [!NOTE]
> [!OBSERVAçãO] **EditMode** pode retornar um valor válido apenas se existir um registro atual. O **EditMode** retornará um erro se [BOF ou EOF](bof-eof-properties-ado.md) for verdadeiro ou se o registro atual tiver sido excluído.


