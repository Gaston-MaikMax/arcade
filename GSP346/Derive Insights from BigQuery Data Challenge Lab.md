<h1 align="center">
🚀  Prepare Data for Looker Dashboards and Reports: Challenge Lab
 || GSP346     🚀
</h1>

### **Solution Video:** [Watch Here]()

### Task 1

```lookml


explore: +airports {
     query: TechCode9{
      dimensions: [city, state]
      measures: [count]
      filters: [airports.facility_type: "HELIPORT^ ^ ^ ^ ^ ^ ^ "]
    }
}

```

### Task 2

```lookml


explore: +airports {
    query: TechCode9{
      dimensions: [facility_type, state]
      measures: [count]
    }
  }

```

### Task 1

```lookml


explore: +flights {
    query: TechCode9{
      dimensions: [aircraft_origin.city, aircraft_origin.state]
      measures: [cancelled_count, count]
    }
}

```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
