---
title: 'Erro do servidor de Internet: Acesso negado'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db78b6f2c51e2e5df918622043e33abc6bc9e674
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463207"
---
# <a name="internet-server-error-access-denied"></a>Erro do servidor de Internet: Acesso negado


**Aplica-se a**: Access 2013 | Office 2013

Se você receber este erro, geralmente significa que o Microsoft Internet Information Services (IIS) retornou o seguinte status:

HTTP\_STATUS\_NEGADOS 401

Certifique-se de que os diretórios acessados pelo IIS têm as permissões adequadas. O RDS pode se comunicar com um servidor Web IIS em qualquer um dos modos de Autenticação de senha: Anônimo, Básico ou Resposta/Desafio NT (chamado de autenticação integrada do Windows no Windows 2000). Além disso, o servidor Web deve ter permissões para o computador da origem de dados se for um computador com Windows NT/Windows 2000.

