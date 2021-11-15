
# 13 - [`Timed.isTimeEnded` returns true if the timer has not been initialized](./`Timed.isTimeEnded`%20returns%20true%20if%20the%20timer%20has%20not%20been%20initialized.md)

`Timed.isTimeEnded` returns true if the timer has not been initialized `Timed` initialization is a 2-step process: 1) `Timed.duration` is set in the constructor 2) `Timed.startTime` is set when the method `_initTimed` is called. Before this second method is called, `isTimeEnded()` calculates remaining time using a `startTime` of 0, resulting in the method returning true for most values, even though the timer has not technically been started.


1.  Recommendation: If Timed has not been initialized, _isTimeEnded_() should return false, or revert
2.  Medium severity finding from [Consensys Diligence Audit of Fei Protocol](https://consensys.net/diligence/audits/2021/01/fei-protocol/#timed-istimeended-returns-true-if-the-timer-has-not-been-initialized)


___
## Slide Screenshot
![013.png](../../images/7.%20Audit%20Findings%20101/013.png)
___
## Slide Text
- 
___
## References
- Youtube Reference
___
## Tags