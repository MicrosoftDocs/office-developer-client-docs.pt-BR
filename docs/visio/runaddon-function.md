---
title: Função RUNADDON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251492
localization_priority: Normal
ms.assetid: 122c1d30-3cb9-7e7d-b4cc-e93ab8e4da4f
description: Executa um complemento ou uma macro em um Microsoft projeto Visual Basic for Applications (VBA).
ms.openlocfilehash: 31ac32c742827311d8aaee4547024ad97d2c48e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772835"
---
# <a name="runaddon-function"></a>Função RUNADDON

Executa um complemento ou uma macro em um Microsoft projeto Visual Basic for Applications (VBA). 
  
## <a name="syntax"></a>Sintaxe

RUNADDON (" *cadeia de caracteres* ") 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |Obrigatório  <br/> |**String** <br/> | O nome de um complemento na coleção **Addons** ou de uma macro em um projeto VBA.  <br/> |
   
## <a name="remarks"></a>Comentários

Se o projeto do documento que contém a chamada de função RUNADDON (ou outro projeto se for referenciado) não tiver uma macro (um procedimento sem argumentos) denominada _cadeia de caracteres_, o Microsoft Visio executa o complemento chamado de _cadeia de caracteres_. Se nenhum complemento chamado de _cadeia de caracteres_ pode ser encontrado, o Visio não faz nada e não relata nenhum erro. (Você pode usar a propriedade **TraceFlags** para monitorar os procedimentos e complementos que o Visio tenta executar). 
  
Quando você chamar um procedimento em um módulo padrão, é recomendável que você prefixo a cadeia de caracteres com o nome do módulo que contém o procedimento (por exemplo, *NomeMódulo. nomeProced*), porque mais de um módulo pode ter um procedimento com o mesmo nome. 
  
Para chamar um procedimento em um projeto diferente do projeto do documento que contém a chamada de função RUNADDON, use a sintaxe *nomeMód* (você deve ter definir explicitamente uma referência ao *NomeDoProjeto* em seu projeto VBA). 
  
> [!NOTE]
>  Iniciando com o Visio 2002, a função RUNADDON não pode executar uma sequência de caracteres contendo código VBA arbitrário. Códigos que tenham anteriormente passado para a função RUNADDON podem ser movidos para um procedimento no projeto VBA de um documento que é chamado a partir da função RUNADDON. 
  
Para obter mais informações sobre a execução de códigos no Visio, consulte [Sobre configurações de segurança e execução de códigos no Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) nesta Referência da ShapeSheet. 
  
Em versões anteriores do Visio, essa função aparece como _RUNADDON. As versões 4.0 e posteriores do Visio aceitam os dois estilos. 
  
## <a name="example-1"></a>Exemplo 1

RUNADDON("Calendar.exe")
  
Inicia um complemento chamado Calendar.exe.
  
## <a name="example-2"></a>Exemplo 2

RUNADDON("Arranjar Formas")
  
Inicia o complemento (implementado em VSL) cujo nome é Arranjar formas.
  
## <a name="example-3"></a>Exemplo 3

RUNADDON("ThisDocument.ReportStatistics")
  
Chama a macro ReportStatistics no módulo **EsteDocumento** no projeto do documento contendo essa chamada de função. 
  
> [!NOTE]
>  Para invocar a macro no módulo **ThisDocument**, anteceda a cadeia de caracteres com "EsteDocumento" como mostrado. 
  
## <a name="example-4"></a>Exemplo 4

RUNADDON (" *ModuleName* . ReportStatistics") 
  
Chama a macro ReportStatistics no *ModuleName* no projeto do documento que contém essa chamada de função. 
  

