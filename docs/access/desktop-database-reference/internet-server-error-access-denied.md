---
title: 'Erro no servidor da Internet: acesso negado'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: af823f46653b3ec83950c2e2cfe639b514196b08
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291252"
---
# <a name="internet-server-error-access-denied"></a>Erro no servidor da Internet: acesso negado


**Aplica-se ao:** Access 2013, Office 2013

Se você receber este erro, geralmente significa que o Microsoft Internet Information Services (IIS) retornou o seguinte status:

HTTP \_ STATUS \_ NEGADO 401

Certifique-se de que os diretórios acessados pelo IIS têm as permissões adequadas. O RDS pode se comunicar com um servidor Web do IIS em execução em qualquer um dos três modos de Autenticação de Senha: Anônimo, Básico ou Desafio/Resposta NT (chamado de autenticação integrada do Windows no Windows 2000). Além disso, o servidor Web deve ter permissões para o computador de fonte de dados se for um computador Com Windows NT/Windows 2000.

