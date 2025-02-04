# Tasks in Hiero

Tasks allow you to automate actions based on specific triggers or schedules. You can set up tasks to execute automatically when certain conditions are met or on a recurring schedule.

## Task Configuration

Each task consists of two main components:

- **Condition**: When the task should execute
- **Action**: What the task should do

Hiero knows how to extract this information from a natural language description, so you can just describe the task in a way that makes sense to you. But if you run into issues, knowing what hiero is looking for can help to achieve the desired result.

### Conditions

Conditions can be time-based, event-based, or a combination of both. The minimum execution period is 5 minutes (e.g. "every 5 minutes" or "every day at 10am" is possible, but "every minute" is not).

Examples of conditions:

- `"5 minutes have passed since the last execution"`
- `"at least one hour has passed since the last execution"`
- `"time of day is after 10pm and this action has not been executed yet today"`
- `"@example_user has tweeted since the last execution"`
- `"the price of ETH has increased at least 5% since the last execution"`
- `"the price of bitcoin is above $100,000"`

### Actions

Actions define what happens when the condition is met. These can range from simple notifications to complex chains of actions.

Examples of actions:

- **Social Media**

  - Quote tweet with specific messages
  - Auto-reply to tweets
  - Create and post creative content

- **Communication**

  - Send email notifications
  - Generate and send news digests
  - Create summary reports

- **Blockchain**
  - Schedule cryptocurrency transfers
  - Create new tokens
  - Monitor and react to blockchain events

## Example Use Cases

1. **Social Media Monitoring**

   ```
   Condition: "@competitor has tweeted since the last execution"
   Action: "reply with a tweet mocking whatever they tweeted"
   ```

   Or, you can describe the task in a way that makes sense to you:
   `Whenever @competitor tweets, reply with a tweet mocking whatever they tweeted`

2. **Automated Content Creation**

   ```
   Condition: "5 minutes have passed since the last execution"
   Action: "Think of a new joke and tweet the joke"
   ```

   Or, you can describe the task in a way that makes sense to you:
   `Every 5 minutes, think of a new joke and tweet the joke`

3. **Scheduled Reports**

   ```
   Condition: "time of day is 9am and this action has not been executed yet today"
   Action: "Send email news digest about AI"
   ```

   Or, you can describe the task in a way that makes sense to you:
   `Every day at 9am, send me an email news digest about AI`

4. **Blockchain Automation**

   ```
   Condition: "7 days have passed since the last execution"
   Action: "Transfer 0.001 ETH to 0x..."
   ```

   Or, you can describe the task in a way that makes sense to you:
   `Once a week, transfer 0.001 ETH to 0x...`

## Limitations

- Maximum number of tasks per user is currently 5
- Minimum execution interval is 5 minutes
- Tasks must have clear, evaluatable conditions

Also, currently users do not have access to the task history, so they cannot see what has been executed and what the result was. If the task is to tweet and a tweet is created, a that is proof of the successful execution. But if the task failed because hiero does not have access to the user's twitter account, there is no way to know that yet. We are working on a solution for this.
