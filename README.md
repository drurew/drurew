I have recently successfully ported several unsupported CANopen batteries to the Victron Cerbo GX ecosystem. If you are struggling to get your specific battery bank communicating with a Victron system, I may be able to help.

To build a driver for a new battery, I typically require either the protocol datasheet or an unencrypted firmware file to reverse-engineer the logic.
Current Support Status:

    Super-B / Redarc: Status: Tested & Working.

    Samsung SDI: Status: Developed (Untested, but built to datasheet specifications).

Additional Tools & Services:

    Battery Aggregator: I’ve developed a standalone service that allows you to run multiple BMS units on a single Cerbo. It includes active charge throttling support. (While Victron has placeholders for aggregation in their codebase, this service fills that gap until they release an official update.)

    Super-B Epsilon Recovery Script: I have developed a script to recover Epsilon batteries stuck in a "Silent Boot Loop" following the v1.3.5 firmware update.

Super-B Epsilon Recovery (The v1.3.5 "Vector Table" Fix) I have a script to patch and recover Epsilon batteries that fail to boot after updating from v1.2.5. The issue is a Vector Table mismatch, not permanent corruption. Have a look at the wiki for the root cause analysis.

Testers are welcome. If you have an unsupported battery or a bricked Epsilon unit, feel free to reach out.
