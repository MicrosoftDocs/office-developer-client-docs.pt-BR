---
title: Propriedade QueryDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ad761c2941cb556ce67c9f716247663220f753f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873688"
---
# <a name="querydefupdatable-property-dao"></a>Propriedade QueryDef.Updatable (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Retorna um valor que indica se você pode alterar um objeto DAO. **Boolean** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . Atualizável

*expressão* Uma variável que representa um objeto **QueryDef** .

## <a name="remarks"></a>Comentários

A propriedade **Updatable** de um objeto **QueryDef** será definida como **True** se a definição da consulta puder ser atualizada, mesmo que o objeto **[Recordset](recordset-object-dao.md)** resultante não seja atualizável.

