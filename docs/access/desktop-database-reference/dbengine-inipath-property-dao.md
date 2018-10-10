---
title: Propriedade DBEngine.IniPath (DAO)
TOCTitle: IniPath Property
ms:assetid: b18cace5-4e53-d011-6373-f4ac64556fd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822009(v=office.15)
ms:contentKeyID: 48547151
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053070
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1bb594ad9866785db3d12f114f6be0eccbbe2289
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463496"
---
# <a name="dbengineinipath-property-dao"></a>Propriedade DBEngine.IniPath (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Define ou retorna informações sobre a chave do Registro do Windows que contém os valores do mecanismo do banco de dados do Microsoft Access (somente em espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . IniPath

*expressão* Uma variável que representa um objeto **DBEngine** .

## <a name="remarks"></a>Comentários

Configure o mecanismo do banco de dados do Microsoft Access com o Registro do Windows. Use o Registro para definir as opções, como DLLs instaláveis do ISAM.

Para essa opção ter efeito, defina a propriedade **IniPath** antes de o aplicativo chamar qualquer outro código do DAO. O escopo dessa configuração está limitado ao aplicativo e não pode ser alterado sem reiniciar o aplicativo.

Também é possível usar o Registro para fornecer os parâmetros de inicialização de alguns drivers dos bancos de dados ISAM instaláveis. Por exemplo, para usar o Paradox versão 4.0, defina a propriedade **IniPath** como uma parte do Registro que contém os parâmetros adequados.

Essa propriedade reconhece qualquer HKEY\_LOCAL\_máquina ou HKEY\_LOCAL\_usuário. Se nenhuma chave raiz for fornecido, o padrão é HKEY\_LOCAL\_máquina.

