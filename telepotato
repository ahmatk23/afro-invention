let item = 0
let potato = 0
input.onButtonPressed(Button.AB, () => {
    potato = 10 + Math.random(21)
})
input.onGesture(Gesture.Shake, () => {
    if (potato) {
        radio.sendNumber(potato)
        item = -1
    }
})
radio.onDataPacketReceived( ({ receivedNumber }) =>  {
    potato = receivedNumber
})
potato = -1
radio.setGroup(1)
basic.forever(() => {
    if (item == 0) {
        basic.showIcon(IconNames.Heart)
    }
    if (item < 0) {
        basic.clearScreen()
    }
    if (potato > 0) {
        basic.showIcon(IconNames.Heart)
        potato += -1
    }
})
