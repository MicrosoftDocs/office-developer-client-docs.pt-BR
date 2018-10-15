---
title: Lançar objetos de modo sistemático
TOCTitle: Systematically releasing objects
ms:assetid: d4cd1d8e-aae6-483b-a4d8-1656171e838d
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623945(v=office.15)
ms:contentKeyID: 55119785
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 812f720b3ebab1100040802d7593548063497297
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406831"
---
# <a name="systematically-releasing-objects"></a>Lançar objetos de modo sistemático

Este tópico resume as recomendações de encerramento dos suplementos para desenvolvedores de suplemento e administradores de TI que usam o Outlook. Para saber mais, confira [alterações de desligamento para o Outlook 2010](https://msdn.microsoft.com/library/ee720183\(v=office.15\)).

## <a name="add-in-shutdown-changes-in-outlook"></a>Alterações de encerramento dos suplementos no Outlook

A partir do Outlook 2010, o Outlook, por padrão, não sinaliza suplementos que estão sendo encerrados. Especificamente, o Outlook não aciona mais os métodos **OnBeginShutdown(Array)** e **OnDisconnection (ext\_DisconnectMode, matriz)** e a interface**IDTExtensibility2** durante o encerramento rápido. Da mesma forma, um suplemento do Outlook, escrito com as ferramentas de desenvolvimento do Office no Visual Studio 2010 ou em versões posteriores, não aciona o método ThisAddin\_desligamento quando o Outlook está sendo desligado. 

O motivo para não acionar esses métodos é que, embora a maioria dos suplementos realize tarefas simples como o lançamento de referências, alguns suplementos fazem chamadas de serviço da Web ou outras operações de longa duração sincronicamente durante esses eventos, isso atrasa significativamente o desligamento do Outlook. Como essa alteração, o Outlook funciona melhor do que anteriormente quando está desligando.

## <a name="recommendations-for-add-in-shutdown-for-developers"></a>Recomendações para o encerramento dos suplementos para desenvolvedores

É importante que os desenvolvedores observem as seguintes recomendações para desligamento de suplemento para garantir que os usuários finais continuem a se beneficiar de uma experiência de desligamento do Outlook rápida e eficaz.

- Suplementos devem continuar implementando os métodos OnBeginShutdown e OnDisconnection ou ThisAddin\_desligamento para lançamento de referências e memória alocada, porque há situações em que os administradores podem reverter para desacelerar o desligamento através da política de grupo. O usuário também pode desconectar manualmente pode o suplemento por meio da caixa de diálogo **suplementos COM**.

- Os desenvolvedores de suplemento só devem executar tarefas que ocorram exatamente durante o desligamento.

- Os desenvolvedores de suplemento devem avaliar o desempenho de seus suplementos em várias situações e em diferentes configurações de registro do Windows que controlam o encerramento do Outlook, e modificar proativamente seus suplementos para trabalhar com o Outlook.

## <a name="recommendations-for-add-in-shutdown-for-it-administrators"></a>Recomendações para o encerramento dos suplementos para administradores de TI

Para administradores de TI, se houver suplementos que já estão implantados em uma empresa e não podem ser atualizados para se tornar compatível com o novo desligamento mecanismo do Outlook, os administradores de TI podem recorrer a algumas das configurações de registro do Windows para reverter o desligamento lento.

### <a name="individual-add-in-setting"></a>Configuração de suplemento individual

Os administradores de TI podem habilitar notificações de desligamento individuais de suplementos do Outlook como parte da implantação do suplemento. Embora você não possa fazer isso por meio da política de grupo, isso será útil se você tiver requisitos de compatibilidade com versões anteriores de suplementos específicos.

Defina essa configuração para cada suplemento através do registro de suplemento adicionar nas seções de registro HKCU HKLM, adicionando outro valor para o registro de suplemento. Digite o seguinte texto em uma única linha:

`HKCU\Software\Microsoft\Office\Outlook\Add-ins\<ProgID>[RequireShutdownNotification]=dword:0x1`

Definir esse valor como 0x1 permite que o suplemento receba chamadas de retorno bloqueadas durante o encerramento do Outlook. Isso tem um impacto no desempenho do desligamento do Outlook e deve ser avaliado como parte de uma implantação. Essa configuração deve ser usada somente se um suplemento tiver problemas significativos de compatibilidade com o novo mecanismo de desligamento. Configurar o valor como 0x0 usa o comportamento padrão do Outlook.

### <a name="global-setting"></a>Configurações globais

Os administradores de TI podem habilitar as notificações de desligamento global para todos os suplementos com política de grupo. Isso é recomendável para organizações que têm um grande número de soluções internas ou computadores que precisam implantar esta configuração para garantir a compatibilidade durante a implementação do Outlook.

Use essa configuração para alterar o mecanismo de encerramento correspondente àquela usado pelo Outlook 2007. Você pode implantar a configuração por meio da política de grupo, por usuário ou por computador. Digite o seguinte texto em uma única linha:

`HKCU\Policies\Microsoft\Office\Outlook\15.0\Options\Shutdown[AddinFastShutdownBehavior]=dword:0x1`

AddinFastShutdownBehavior como 0x1 permite que as notificações de desligamento para todos os suplementos. A configuração do valor para 0x0 usa o comportamento padrão do Outlook.

