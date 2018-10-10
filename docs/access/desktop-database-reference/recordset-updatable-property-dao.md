---
title: Propriedade Recordset.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 2d4bdcef-1b10-b542-ce0f-6172c271131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192110(v=office.15)
ms:contentKeyID: 48543968
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 77f3c7331e42d0f9a63a0f87330f8acbc49a646b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462409"
---
# <a name="recordsetupdatable-property-dao"></a>Propriedade Recordset.Updatable (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Retorna um valor que indica se você pode alterar um objeto DAO. **Boolean** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . Atualizável

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="remarks"></a>Comentários

Objetos Recordset do tipo instantâneo e somente de encaminhamento sempre retornará **False**.

Muitos tipos de objetos podem conter campos não podem ser atualizados. Por exemplo, crie um objeto **Recordset** do tipo dynaset no qual somente alguns campos podem ser alterados. Esses campos podem ser consertados ou conter dados que são incrementados automaticamente ou o dynaset pode resultar de uma consulta que combina tabelas atualizáveis e não atualizáveis.

Se o objeto contém campos somente leitura, o valor da propriedade **Updatable** será **False**. Quando um ou vários campos são atualizáveis, o valor da propriedade será **True**. Você pode editar somente os campos atualizáveis. Ocorrerá um erro interceptável, se você tentar atribuir um novo valor a um campo somente leitura.

Como um objeto atualizável pode conter campos somente leitura, verifique a propriedade **DataUpdatable** de cada campo na coleção **Fields** de um objeto **Recordset** antes de editar um registro.

