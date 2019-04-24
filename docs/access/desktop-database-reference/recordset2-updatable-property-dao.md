---
title: Propriedade Recordset2. upDatable (DAO)
TOCTitle: Updatable Property
ms:assetid: ad8184b6-ffe3-dde6-ddee-4b23cdaa9c59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821726(v=office.15)
ms:contentKeyID: 48547041
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b6e6f2a20b4779259b80eff1fc152abe3698217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309159"
---
# <a name="recordset2updatable-property-dao"></a>Propriedade Recordset2. upDatable (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Retorna um valor que indica se você pode alterar um objeto DAO. **Boolean** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . Atualizável

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="remarks"></a>Comentários

Os objetos Recordset do tipo instantâneo e somente de encaminhamento sempre retornam **false**.

Muitos tipos de objetos podem conter campos não podem ser atualizados. Por exemplo, crie um objeto **Recordset** do tipo dynaset no qual somente alguns campos podem ser alterados. Esses campos podem ser consertados ou conter dados que são incrementados automaticamente ou o dynaset pode resultar de uma consulta que combina tabelas atualizáveis e não atualizáveis.

Se o objeto contém campos somente leitura, o valor da propriedade **Updatable** será **False**. Quando um ou vários campos são atualizáveis, o valor da propriedade será **True**. Você pode editar somente os campos atualizáveis. Ocorrerá um erro interceptável, se você tentar atribuir um novo valor a um campo somente leitura.

Como um objeto atualizável pode conter campos somente leitura, verifique a propriedade **DataUpdatable** de cada campo na coleção **Fields** de um objeto **Recordset** antes de editar um registro.

