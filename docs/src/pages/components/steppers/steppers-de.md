---
title: Stepper React-Komponente
components: MobileStepper, Step, StepButton, StepConnector, StepContent, StepIcon, StepLabel, Stepper
---

# Stepper

<p class="description">Steppers convey progress through numbered steps. It provides a wizard-like workflow.</p>

[Stepper](https://material.io/archive/guidelines/components/steppers.html) zeigen den Fortschritt durch eine Folge logischer und nummerierter Schritte an. Sie können auch zur Navigation verwendet werden. Steppers können eine vorübergehende Rückmeldung anzeigen, nachdem ein Schritt gespeichert wurde.

- **Types of Steps**: Editable, Non-editable, Mobile, Optional
- **Types of Steppers**: Horizontal, Vertical, Linear, Non-linear

> **Note:** Steppers are no longer documented in the [Material Design guidelines](https://material.io/), but Material-UI will continue to support them.

## Horizontal Stepper

### Linear

Der `Stepper` kann gesteuert werden, indem der aktuelle Schrittindex (auf Null basierend) als `activeStep` Eigenschaft übergeben wird. Die `Stepper-` Ausrichtung wird mithilfe der Eigenschaft `orientation` gesetzt.

Dieses Beispiel zeigt auch die Verwendung eines optionalen Schritt durch setzten der `optional` Eigenschaft auf der zweiten `Step` Komponente. Beachten Sie, dass Sie selbst entscheiden müssen, wann ein optionaler Schritt übersprungen wird. Wenn Sie dies für einen bestimmten Schritt festgelegt haben, müssen Sie `complete={false}` setzten, um anzuzeigen, dass der Index des aktiven Schritts den optionalen Schritt überschritten hat, jedoch nicht wirklich abgeschlossen ist.

{{"demo": "pages/components/steppers/HorizontalLinearStepper.js"}}

### Linear - Alternative Label

Labels can be placed below the step icon by setting the `alternativeLabel` prop on the `Stepper` component.

{{"demo": "pages/components/steppers/HorizontalLinearAlternativeLabelStepper.js"}}

### Anpasster Stepper

Hier ist ein Beispiel zum Anpassen der Komponente. Mehr dazu erfahren Sie auf der [Überschreibungsdokumentationsseite](/customization/components/).

{{"demo": "pages/components/steppers/CustomizedSteppers.js"}}

### Nicht linear

Mit nichtlinearen Steppern können Benutzer an jedem Punkt einen mehrstufigen Fluss einsteigen.

Dieses Beispiel ähnelt dem regulären horizontalen Stepper, mit der Ausnahme, dass Schritte nicht mehr automatisch auf `=disabled={true}` basierend auf der Eigenschaft `activeStep` gesetzt werden.

Wir haben den `StepButton` hier verwendet, um anklickbare Schrittbeschriftungen zu demonstrieren sowie das Eigenschaft `completed`. Da Schritte auf nicht lineare Weise aufgerufen werden können, müssen Sie dies selbst implementieren und festzulegen, wann alle Schritte abgeschlossen sind (oder auch wenn sie abgeschlossen sein müssen).

{{"demo": "pages/components/steppers/HorizontalNonLinearStepper.js"}}

### Non Linear - Alternative Label

Labels can be placed below the step icon by setting the `alternativeLabel` prop on the `Stepper` component.

{{"demo": "pages/components/steppers/HorizontalNonLinearAlternativeLabelStepper.js"}}

### Non Linear - Error Step

{{"demo": "pages/components/steppers/HorizontalNonLinearStepperWithError.js"}}

## Vertikaler Stepper

{{"demo": "pages/components/steppers/VerticalLinearStepper.js"}}

## Mobile Stepper

Diese Komponente implementiert einen kompakten Stepper, der für ein mobiles Gerät geeignet ist. Siehe [Mobile steps](https://material.io/archive/guidelines/components/steppers.html#steppers-types-of-steps) zur Inspiration.

### Text

This is essentially a back/next button positioned correctly. You must implement the textual description yourself, however, an example is provided below for reference.

{{"demo": "pages/components/steppers/TextMobileStepper.js"}}

### Text with Carousel effect

Diese Demo ist der vorherigen sehr ähnlich, der Unterschied besteht in der Verwendung von [react-swipeable-views](https://github.com/oliviertassinari/react-swipeable-views), um den Übergang von Schritten zu realisieren.

{{"demo": "pages/components/steppers/SwipeableTextMobileStepper.js"}}

### Dots

Verwenden Sie Punkte, wenn die Anzahl der Schritte nicht groß ist.

{{"demo": "pages/components/steppers/DotsMobileStepper.js"}}

### Fortschritt (Progress)

Verwenden Sie eine Fortschrittsleiste, wenn viele Schritte vorhanden sind oder wenn Schritte eingefügt werden müssen (basierend auf den Antworten auf frühere Schritte).

{{"demo": "pages/components/steppers/ProgressMobileStepper.js"}}