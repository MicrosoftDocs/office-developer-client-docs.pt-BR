---
title: Propriedade TableDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 44f24e68b60f69304a167d2b9b5ce0b4b0e69b11
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465300"
---
# <a name="tabledefupdatable-property-dao"></a>Propriedade TableDef.Updatable (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Retorna um valor que indica se você pode alterar um objeto DAO. **Boolean** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . Atualizável

*expressão* Uma variável que representa um objeto **TableDef** .

## <a name="remarks"></a>Comentários

A definição da propriedade **Updatable** será sempre **True** para um objeto **TableDef** recentemente criado e **False** para um objeto **TableDef** vinculado. Um novo objeto **TableDef** pode ser acrescentado somente a um banco de dados para o qual o usuário atual tiver permissão de gravação.

